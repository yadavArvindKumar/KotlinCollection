import kotlin.random.Random

class BinarySearch {
    private var counter = 0
    private val maxGuess = 50
    fun main() {
        val min = 1
        val max = 1000000
        val numberToBeGuessed: Int = Random.nextInt(min, max)
        findNumberInRange(min, max, numberToBeGuessed)
    }

    private fun findNumberInRange(min: Int, max: Int, numberToBeGuessed: Int) {
        val number: Int = finNumberUsingBinarySearch(min, max, numberToBeGuessed)
        if (number > 0) {
            println("number is - $number")
            println("number of guess is - $counter")
        } else {
            println("Number not found")
        }
    }

    private fun finNumberUsingBinarySearch(min: Int, max: Int, numberToBeGuessed: Int): Int {
        while (counter < maxGuess) {
            val mid = (min + max) / 2
            counter++
            when {
                numberToBeGuessed == mid -> return mid
                numberToBeGuessed > mid -> return finNumberUsingBinarySearch(
                    mid + 1,
                    max,
                    numberToBeGuessed
                )
                numberToBeGuessed < mid -> return finNumberUsingBinarySearch(
                    min, mid - 1, numberToBeGuessed
                )
            }
        }
        return -1
    }
}
