Routing:
con la libreria de Routing puedes tener diferentes URLs y mostrar
diferentes componentes, asi como regtringir el acceso a ciertas paginas

Librerias:
React Router V6 conformado por dos ( Reach-Router y Remix-Run)
React Location

Gatsby y Next.js (tienen sus propias librerias)

React Router
manejo de multiples paginas con url
--> npm i react-router-dom

usar formulario
--> npm i formik yup

import {BrowserRouter, Routes, Route} from 'react-router-dom'
import { Outlet, Link } from "react-router-dom";

-BrowserRouter: registra nuevos enpoints y que cargue nuevos componentes
-Routes: todas las rutas van a estar dentro de este componente puede ser singular o multiple rutas
-Outlet: Esto permite que la interfaz de usuario anidada se muestre cuando se representan las rutas secundarias. Si la ruta principal coincide exactamente, generará una ruta de índice secundaria o nada si no hay una ruta de índice.
<BrowserRouter>
    <Routes>
      <Route>
        <Route/> // singular de una sola ruta
      </Route>
    </Routes>
  </Routes>
</BrowserRouter>

<BrowserRouter>
    <Routes>
      <Route>
        <Route/> // singular de una sola ruta
      </Route>
      <Route>
        <Route/> // multiples rutas
        <Route/> // multiples rutas
        <Route/> // multiples rutas
        <Route/> // multiples rutas
        <Route/> // multiples rutas
        <Route/> // multiples rutas
      </Route>
    </Routes>
  </Routes>
</BrowserRouter>

Cada Route va con un PATH que indica la ruta a la que se va ingresar
seguido de un ELEMENT ={<Componete/>} indicando el componenete  que se va mostrar
<BrowserRouter>
    <Routes>
      <Route path="/clientes" element={<Componente/>}>
        <Route/>
      </Route>
    </Routes>
  </Routes>
</BrowserRouter>

para visualisar el contenido del componete accesido 
se añana la palabra INDEX indicando que esa va ser la parte principal del componente accedio
<BrowserRouter>
    <Routes>
      <Route path="/clientes" element={<Componente/>}>
        <Route  index element={<Inicio/>}/>
      </Route>
    </Routes>
  </Routes>
</BrowserRouter>




para los enlaces ya no se utiliza la etiqueta <a> </a>
en su lugar ahora se utiliza <Link> </Link>

para ingresar la ruta no se usa href='/enlaces'
en su lugar se utiliza to='/enlaces'
