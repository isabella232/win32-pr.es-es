---
title: Adición del atributo ContentDistributor
description: Adición del atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player tiendas en línea, agregar el atributo ContentDistributor
- tiendas en línea, agregar atributo ContentDistributor
- Escriba 1 tiendas en línea, agregando atributo ContentDistributor
- Escriba 2 tiendas en línea, agregando atributo ContentDistributor
- Windows Media Player tiendas en línea, atributo ContentDistributor
- tiendas en línea, atributo ContentDistributor
- tipo 1 almacenes en línea, atributo ContentDistributor
- tipo 2 tiendas en línea, atributo ContentDistributor
- adición del atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357128"
---
# <a name="adding-the-contentdistributor-attribute"></a>Adición del atributo ContentDistributor

Cuando el usuario intenta reproducir contenido de la tienda en línea o copiar el contenido en un CD o un dispositivo, Windows Media Player llama a determinados métodos en el objeto COM. Para ello, el reproductor necesita una manera de diferenciar el contenido de otros proveedores de tiendas en línea. Al agregar el nombre de la clave de la tienda en línea como valor de **ContentDistributor** (que es un alias para el atributo Windows Media Format SDK denominado **WM/ContentDistributor**) en el contenido basado en Windows Media, asegúrese de que el reproductor puede identificar el contenido asociado a su servicio.

La adición de un valor para **ContentDistributor** también garantiza que Windows Media Player creará un nodo en la biblioteca para el contenido que proporcione. Consulte [integración de bibliotecas](library-integration.md).

Este valor se puede especificar de dos maneras:

-   Use el modelo de objetos de Media Player de Windows. Al hacerlo, Windows Media Player agrega el valor especificado a la base de datos de biblioteca. Finalmente, el reproductor también escribirá el valor de atributo en el archivo multimedia digital.
-   Use el SDK de Windows Media Format para agregar mediante programación el atributo **WM/ContentDistributor** . Al hacerlo, Windows Media Player lee el valor del atributo y lo agrega a la base de datos cuando se agrega el archivo multimedia digital a la biblioteca.

Al crear el objeto COM de la tienda en línea, el valor del atributo de archivo establecido para **ContentDistributor** y el valor asignado a la constante KszContentDistributorID en YourProject. h deben coincidir exactamente. Recuerde que especificó este valor constante para el objeto COM al crear el proyecto mediante el Asistente para proyectos. Puede cambiar este valor manualmente. Asegúrese de usar una cadena que identifique de forma única el servicio.

## <a name="using-the-windows-media-player-object-model"></a>Usar el modelo de objetos de Media Player de Windows

Para especificar un valor para **ContentDistributor** con el modelo de objetos de Media Player de Windows, use el método [media. setItemInfo](media-setiteminfo.md) . En el ejemplo de código siguiente se especifica el valor "Proseware" para **ContentDistributor** para el elemento multimedia que se está reproduciendo actualmente:


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>Usar el SDK de Windows Media Format

El SDK de Windows Media Player incluye un archivo de C++ de ejemplo denominado SetContentDistributor. cpp, que muestra cómo usar el SDK de Windows Media Format 9 series para agregar el atributo **WM/ContentDistributor** . Puede buscar este archivo de ejemplo en la carpeta denominada Metadata (metadatos) en la que instaló el SDK. Para usar este código debe seguir estos pasos:

1.  Instale el SDK de Windows Media Format 9 series y configure el tiempo de ejecución como se describe en la documentación de.
2.  Cree un nuevo proyecto de C++ vacío en Visual Studio y agregue el archivo de ejemplo denominado SetContentDistributor. cpp al proyecto.
3.  Agregue la ruta de acceso a las carpetas de biblioteca de SDK de Windows Media Format 9 series a la lista de rutas de acceso de archivo. En el menú **Herramientas** , elija **Opciones**.
4.  En el cuadro de diálogo **Opciones** , haga clic en **proyectos** y, a continuación, haga clic en **directorios de VC + +**.
5.  En el cuadro de lista desplegable **Mostrar directorios para** , haga clic en **archivos de biblioteca**.
6.  Use los botones para agregar las rutas de acceso a los cuadros de lista.
7.  Abra el cuadro de diálogo páginas de propiedades del proyecto. Seleccione **propiedades de configuración**, **enlazador** y, a continuación, **Escriba**. Escriba "wmvcore. lib" en el cuadro de texto **dependencias adicionales** .

El código de ejemplo crea un programa de línea de comandos. Los argumentos que se proporcionan al ejecutar el programa especifican la ruta de acceso al archivo multimedia digital que se va a modificar y una cadena para el valor del atributo **ContentDistributor** . El código usa **IWMHeaderInfo:: setAttribute** para agregar el atributo al archivo especificado. Puede usar este ejemplo tal como está o usarlo como punto de partida para su propio programa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




