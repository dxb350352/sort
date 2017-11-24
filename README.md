可以排序基本数据类型的数组和结构体数组

func main() {

	var arr = []int{3, 2, 1, 4, 5}
	sort.Sort(arr, false)
	fmt.Println(arr)//[5 4 3 2 1]
	type Test struct {
		Id   int
		Name string
	}
	var arrt []Test
	arrt = append(arrt, Test{1, "A"})
	arrt = append(arrt, Test{1, "C"})
	arrt = append(arrt, Test{2, "A"})
	arrt = append(arrt, Test{2, "B"})
	arrt = append(arrt, Test{1, "B"})
	arrt = append(arrt, Test{2, "C"})
	sort.Sort(arrt, true, "Name", "Id")
	fmt.Println(arrt)//[{1 A} {2 A} {1 B} {2 B} {1 C} {2 C}]
}