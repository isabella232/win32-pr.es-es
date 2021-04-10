---
description: El SDK de Windows Search proporciona un ensamblado de interoperabilidad para trabajar con objetos del modelo de objetos componentes (COM) expuestos por Windows Search y otros programas en las interfaces y clases mediante código administrado.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Uso de código administrado con datos de shell y Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153991"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Uso de código administrado con datos de shell y Windows Search

El SDK de Windows Search proporciona un ensamblado de interoperabilidad para trabajar con objetos del modelo de objetos componentes (COM) expuestos por Windows Search y otros programas en las interfaces y clases mediante código administrado. El ensamblado de interoperabilidad está firmado digitalmente por Microsoft y puede encontrarse con los [ejemplos de Windows Search](-search-samples-ovw.md).

Este tema se organiza de la siguiente manera:

-   [Uso de la API de Windows CodePack](#using-the-windows-api-codepack)
    -   [Obtener acceso a los resultados del índice](#accessing-index-results)
    -   [Aplicación de ejemplo que usa la API de Windows Codepack](#sample-application-using-the-windows-api-codepack)
-   [Temas relacionados](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Uso de la API de Windows CodePack

Si está trabajando en el entorno de Microsoft .NET, use el [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) para obtener los resultados de la búsqueda o simplemente examine el espacio de nombres. El [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) proporciona una colección de elementos de Shell que básicamente son contenedores en torno a la [interfaz IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa. Puede recorrer en iteración esta colección y obtener los distintos valores de propiedad de forma similar a como se enumerarían los resultados en una tabla de una consulta de vinculación e incrustación de base de datos (OLE DB).

En el fragmento de código siguiente se muestra cómo recorrer en iteración los elementos de búsqueda y obtener los valores de propiedad para cada uno.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Obtener acceso a los resultados del índice

Puede tener acceso a los resultados del índice a través de OLE DB o del modelo de datos de Shell. Hay ventajas y desventajas con cualquiera de estos enfoques. Una ventaja es que OLE DB y Lenguaje de consulta estructurado (SQL) están familiarizados con los programadores de bases de datos. Otras ventajas son el mejor control sobre el rendimiento cuando se consulta solo el indexador y el acceso a una funcionalidad adicional, como la capacidad de buscar los resultados anteriores en un conjunto de filas nuevo rápidamente.

Las ventajas del modelo de datos de Shell son que abstrae entre diferentes orígenes de información como OpenSearch y proporciona acceso a funcionalidad adicional, como miniaturas y controladores de propiedades. Además, el modelo de objetos de Shell requiere una compatibilidad especial para los resultados que no son de nombre de archivo, como los elementos de correo y los resultados de OneNote, o para cualquier elemento que resida en el índice del usuario. Tenga en cuenta que en Shell [KNOWNFOLDERID](../shell/knownfolderid.md) es el ámbito de carpeta conocido para el contenido indexado local. Para obtener más información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Los orígenes de datos de OpenSearch no se exponen a través de OLE DB para la búsqueda federada en Windows 7 y versiones posteriores. Por esta razón, se recomienda que considere la posibilidad de escribir un proveedor LINQ para el espacio de nombres de Shell en lugar de usar OLE DB para tener acceso a los resultados del indexador. Para obtener más información, vea [Tutorial: crear un proveedor LINQ de IQueryable](/previous-versions/bb546158(v=vs.140)).

### <a name="sample-application-using-the-windows-api-codepack"></a>Aplicación de ejemplo que usa la API de Windows Codepack

La captura de pantalla siguiente representa un simulacro de una aplicación de ejemplo creada con el [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).

![captura de pantalla de la aplicación de reproductor de media que muestra mensajes de correo electrónico](images/folderid-searchhome.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Interoperabilidad entre lenguajes](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
