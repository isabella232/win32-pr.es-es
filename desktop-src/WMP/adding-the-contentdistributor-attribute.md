---
title: Agregar el atributo ContentDistributor
description: Agregar el atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Reproductor de Windows Media en línea, agregar el atributo ContentDistributor
- tiendas en línea, agregar el atributo ContentDistributor
- tiendas en línea de tipo 1, agregar el atributo ContentDistributor
- tipo 2 tiendas en línea, agregar el atributo ContentDistributor
- Reproductor de Windows Media en línea, atributo ContentDistributor
- tiendas en línea, atributo ContentDistributor
- type 1 online stores,ContentDistributor attribute
- tipo 2 tiendas en línea, atributo ContentDistributor
- agregar el atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374314"
---
# <a name="adding-the-contentdistributor-attribute"></a>Agregar el atributo ContentDistributor

Cuando el usuario intenta reproducir contenido de la tienda en línea o copiarlo en un CD o dispositivo, Reproductor de Windows Media llama a determinados métodos en el objeto COM. Para ello, el reproductor necesita una manera de diferenciar el contenido del de otros proveedores de tiendas en línea. Al agregar el nombre de la clave del almacén en línea como valor del atributo **ContentDistributor** (que es un alias del atributo del SDK de formato multimedia de Windows denominado **WM/ContentDistributor)** al contenido basado en multimedia de Windows, se asegura de que el Reproductor pueda identificar el contenido asociado con el servicio.

Agregar un valor para **ContentDistributor** también garantiza que Reproductor de Windows Media creará un nodo en la biblioteca para el contenido que proporcione. Vea [Integración de bibliotecas.](library-integration.md)

Puede especificar este valor de dos maneras:

-   Use el Reproductor de Windows Media de objetos. Al hacerlo, Reproductor de Windows Media agrega el valor especificado a la base de datos de biblioteca. Finalmente, el reproductor también escribirá el valor del atributo en el archivo multimedia digital.
-   Use el SDK Windows Media Format para agregar mediante programación el **atributo WM/ContentDistributor.** Al hacerlo, Reproductor de Windows Media el valor del atributo y lo agrega a la base de datos cuando el archivo multimedia digital se agrega a la biblioteca.

Al crear el objeto COM de la tienda en línea, el valor del atributo de archivo establecido para **ContentDistributor** y el valor asignado a la constante kszContentDistributorID en YourProject.h deben coincidir exactamente. Recuerde que especificó este valor constante para el objeto COM al crear el proyecto mediante el Asistente para proyectos. Puede cambiar este valor manualmente. Asegúrese de usar una cadena que identifique de forma única el servicio.

## <a name="using-the-windows-media-player-object-model"></a>Usar el modelo Reproductor de Windows Media objetos

Para especificar un valor para **ContentDistributor** mediante el Reproductor de Windows Media de objetos, use el [método Media.setItemInfo.](media-setiteminfo.md) El código de ejemplo siguiente especifica el valor "Proseware" para **ContentDistributor** para el elemento multimedia que se reproduce actualmente:


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



## <a name="using-the-windows-media-format-sdk"></a>Uso del SDK Windows Media Format

El SDK de Reproductor de Windows Media incluye un archivo de C++ de ejemplo, denominado SetContentDistributor.cpp, que muestra cómo usar el SDK de la serie Windows Media Format 9 para agregar el atributo **WM/ContentDistributor.** Puede encontrar este archivo de ejemplo en la carpeta denominada Metadatos donde instaló el SDK. Para usar este código, debe seguir estos pasos:

1.  Instale el SDK Windows Media Format 9 y configure el entorno de ejecución como se describe en la documentación.
2.  Cree un nuevo proyecto de C++ vacío en Visual Studio y agregue el archivo de ejemplo denominado SetContentDistributor.cpp al proyecto.
3.  Agregue la ruta de acceso a las Windows lib del SDK de la serie Media Format 9 a la lista de rutas de acceso de archivo. En el menú **Herramientas** , elija **Opciones**.
4.  En el cuadro **de diálogo** Opciones , haga clic **en Proyectos** y, a continuación, haga clic **VC++ directorios**.
5.  En el **cuadro de lista desplegable Mostrar** directorios para , haga clic en Archivos de **biblioteca**.
6.  Use los botones para agregar las rutas de acceso a los cuadros de lista.
7.  Abra el cuadro de diálogo páginas de propiedades del proyecto. Elija **Propiedades de configuración**, luego **Vinculador** y, a continuación, **Entrada.** Escriba "wmvcore.lib" en el cuadro **de texto Dependencias** adicionales.

El código de ejemplo crea un programa de línea de comandos. Los argumentos que se proporcionan al ejecutar el programa especifican la ruta de acceso al archivo multimedia digital que se va a modificar y una cadena para el valor del atributo **ContentDistributor.** El código usa **IWMHeaderInfo::SetAttribute** para agregar el atributo al archivo especificado. Puede usar este ejemplo tal y como está o usarlo como punto de partida para su propio programa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




