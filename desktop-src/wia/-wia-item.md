---
description: Windows Los dispositivos de hardware de adquisición de imágenes (WIA) se representan como árboles jerárquicos de objetos Item. El elemento raíz de este árbol representa el propio dispositivo, mientras que los elementos secundarios representan imágenes, carpetas o exploraciones.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Objeto Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 2b5b32603f334148fede3bc2866367817fd3dcd5ab33aaa40bab84fe3cf49624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208938"
---
# <a name="item-object"></a>Objeto Item

Windows Los dispositivos de hardware de adquisición de imágenes (WIA) se representan como árboles jerárquicos de **objetos Item.** El elemento raíz de este árbol representa el propio dispositivo, mientras que los elementos secundarios representan imágenes, carpetas o exploraciones.

Use el **objeto Item** para transferir datos a un archivo, para navegar por el árbol de elementos de un dispositivo determinado o para recuperar información sobre una imagen o un dispositivo.

## <a name="members"></a>Miembros

El **objeto Item** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Item** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | El [**método GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) del objeto **Item** muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | El [**método GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) del **objeto Item** usa el identificador de una propiedad de elemento para devolver su valor.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | El [**método TakePicture**](-wia-iwiadispatchitem-takepicture.md) del objeto **Item** hace que un dispositivo de cámara digital tome una imagen y devuelve un objeto **Item** que representa la imagen resultante. Este método solo se aplica a los dispositivos de cámara digital.<br/> |
| [**Transferencia**](-wia-iwiadispatchitem-transfer.md)             | El [**método Transfer**](-wia-iwiadispatchitem-transfer.md) del objeto **Item** transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Propiedades

El **objeto Item** tiene estas propiedades.



| Propiedad                                                                    | Tipo de acceso          | Descripción                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Solo lectura<br/> | La [**propiedad Children**](-wia-iwiadispatchitem-children.md) del objeto **Item** recupera una colección de **objetos Item.** Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Solo lectura<br/> | Recupera el estado de conexión del dispositivo. Esta propiedad solo se aplica a los elementos de tipo device (elementos raíz). Los valores posibles son "connected", "disconnected" o **NULL** (si esta propiedad no se aplica al elemento). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Solo lectura<br/> | Recupera la versión de firmware del dispositivo. Esta propiedad solo se aplica a los elementos de tipo device (elementos raíz). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Solo lectura<br/> | Recupera el nombre completo del elemento tal como aparece en la interfaz de usuario. <br/>                                                                                                                                                                                    |
| [**Alto**](-wia-iwiadispatchitem-height.md)<br/>                   | Solo lectura<br/> | Alto, en píxeles, del elemento. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Solo lectura<br/> | Tipo de este elemento. <br/>                                                                                                                                                                                                                          |
| [**Nombre**](-wia-iwiadispatchitem-name.md)<br/>                       | Solo lectura<br/> | Nombre del elemento tal como aparece en la interfaz de usuario. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Solo lectura<br/> | Alto, en píxeles, de las imágenes producidas por esta cámara digital. Solo se aplica a las cámaras digitales. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Solo lectura<br/> | Ancho, en píxeles, de las imágenes producidas por esta cámara digital. Solo se aplica a las cámaras digitales. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Solo lectura<br/> | Alto, en píxeles, de la imagen en miniatura. Esta propiedad devuelve -1 si este elemento no admite miniaturas. <br/>                                                                                                                               |
| [**Miniatura**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Solo lectura<br/> | Ruta de acceso y nombre de archivo de la imagen en miniatura. Esta propiedad es **NULL** si el elemento no admite miniaturas o si no se puede crear una ruta de acceso. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Solo lectura<br/> | Ancho, en píxeles, de la imagen en miniatura. Esta propiedad devuelve -1 si este elemento no admite miniaturas. <br/>                                                                                                                                |
| [**Time**](-wia-iwiadispatchitem-time.md)<br/>                       | Solo lectura<br/> | La hora actual. Solo se aplica a los dispositivos. <br/>                                                                                                                                                                                                      |
| [**Ancho**](-wia-iwiadispatchitem-width.md)<br/>                     | Solo lectura<br/> | Ancho, en píxeles, del elemento. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentarios

### <a name="creationaccess-functions"></a>Funciones de \\ acceso de creación

Use cualquiera de las siguientes opciones para recuperar una referencia al objeto :



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Crear**](-wia-iwiadeviceinfo-create.md)

[**Crear**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




