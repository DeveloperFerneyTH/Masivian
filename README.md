# Masivian
1. Entrar a la carpeta MasivianProject y ejecutar el archivo MasivianProject.sln en VS 2017.
2. Se debe dejar como projecto principal el projecto MasivianProject en caso que no este como principal.
3. Una vez ejecutado el proyecto se subira una api, la cual se debe tomar el nombre del servidor (localhost en caso que se ejecute local) y el puerto seguido de la ruta Api/GetAncestor, Ej: http://localhost:3787/Api/GetAncestor.
4. Copiar la ruta completa en una herramienta de prueba de servicios como Postman y utilizar el siguiente formato Json:
{
  "Parent": 70,
  "Child1": 45,
  "Child2": 17,
  "Nodes": [
    {
      "ParentLv1": "80",
      "NodeLv1": "45, 14, 93",
      "ParentLv2": "93",
      "NodeLv2": "21, 30, 17"
    },
    {
      "ParentLv1": "60",
      "NodeLv1": "58, 35, 12",
      "ParentLv2": "58",
      "NodeLv2": "78, 84, 53"
    }
  ]
}

Nota: todos los valores pueden cambiar y se pueden adicionar tantos nodes se requieran siempre y cuando cumplan con la estructura dada.

5. Realizar la petición.

# Prueba desde Proyecto de pruebas unitarias
1. Una vez abierta la solución, esta cuenta con un proyecto de pruebas unitarias para ejecutarlas desde visual estudio (MasivianProject.Tests).
2. Se debe abrir el TestExplorer desde el VS y ejecutar todas las pruebas diseñadas allí.
3. Para modificación de data se debe entrar a la clase TreeTest.cs desde la carpeta BI en la solución.
4. Esta clase tendra un metodo el cual se divide en 3 regiones, la región para modificar el arbol y la respuesta esperada se llama Arrange.
5. Compilar el proyecto y volver a ejecutar las pruebas.
