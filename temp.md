Methods for handling response data:

1. `response.json()`: Returns a promise that resolves with the JSON representation of the response body.
2. `response.text()`: Returns a promise that resolves with the text representation of the response body.
3. `response.blob()`: Returns a promise that resolves with a `Blob` representing the response body (useful for binary data like images).
4. `response.arrayBuffer()`: Returns a promise that resolves with an `ArrayBuffer` containing the response body (useful for working with binary data).
5. `response.formData()`: Returns a promise that resolves with a `FormData` object (useful for handling form data submissions).
6. `response.clone()`: Creates a clone of the response object.

const fetchText = async (url, options) => await (await fetch(url, options)).text()
const fetchJson = async (url, options) => await (await fetch(url, options)).json()
const fetchBlob = async (url, options) => await (await fetch(url, options)).blob()
const fetchArrayBuffer = async (url, options) => await (await fetch(url, options)).arrayBuffer()
const fetchFormData = async (url, options) => await (await fetch(url, options)).formData()



### Inspection Property
`response.headers()`
Returns a `Headers` object containing the headers of the response. You can use `get()` and other methods on the `Headers` object to access and inspect individual headers.





### Typescript

``` TypeScript


const fetchText = async (url: string, options?: RequestInit): Promise<string> => await (await fetch(url, options)).text()

const fetchJson = async <T>(url: string, options?: RequestInit): Promise<T> => await (await fetch(url, options)).json()

const fetchBlob = async (url: string, options?: RequestInit): Promise<Blob> => await (await fetch(url, options)).blob()

const fetchArrayBuffer = async (url: string, options?: RequestInit): Promise<ArrayBuffer> => await (await fetch(url, options)).arrayBuffer()

const fetchFormData = async (url: string, options?: RequestInit): Promise<FormData> => await (await fetch(url, options)).formData()





```
