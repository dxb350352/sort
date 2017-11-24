

func main() {
	var arr = []int{3, 2, 1, 4, 5}
	sort.Sort(arr, false)
	fmt.Println(arr)
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
	fmt.Println(arrt)
}