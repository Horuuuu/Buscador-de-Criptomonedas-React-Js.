<h3>Buscador de precio de criptomonedas con Api de geckocoin.com</h3>

Dos componentes :
<ul>
  <li>TableCoins:para la tabla de las monedas</li>
  <li>CoinsRow:para las filas de la tabla</li>
  
![](img/cripto.jpg)

Para la petición a la Api usé la biblioteca <strong> Axios</strong> y para que se ejecuten los datos inmediatamente cuando carga la aplicacion usé <strong>useEffect</strong> .
  
```
  
  const getData =  async () =>{
  const res= await axios.get("https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1")
  console.log(res.data)
  setCoins(res.data) }
  useEffect(() =>{
    getData()
  },[] )
 
  ```
  
  La tabla la hice con las clases de **Bootstrap** ,
  primero usé el metodo <strong>map</strong> para que recorra cada objeto de la api y generé una fila por cada uno.Luego  para renderizarlo usé las propiedades que tiene cada objeto
  
  
  
![](img/stack.jpg)
