---
description: Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) se representan como árboles jerárquicos de objetos de elementos. El elemento raíz de este árbol representa el propio dispositivo, mientras que los elementos secundarios representan imágenes, carpetas o bancos de digitalización.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Objeto de elemento
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
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810784"
---
# <a name="item-object"></a>Objeto de elemento

Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) se representan como árboles jerárquicos de objetos de **elementos** . El elemento raíz de este árbol representa el propio dispositivo, mientras que los elementos secundarios representan imágenes, carpetas o bancos de digitalización.

Use el objeto **Item** para transferir datos a un archivo, para navegar por el árbol de elementos de un dispositivo determinado o para recuperar información acerca de una imagen o un dispositivo.

## <a name="members"></a>Miembros

El objeto de **elemento** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **elemento** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | El método [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) del objeto **Item** muestra un cuadro de diálogo que permite al usuario seleccionar imágenes y audio para transferir desde un dispositivo.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | El método [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) del objeto **Item** usa el identificador de una propiedad Item para devolver su valor.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | El método [**TakePicture**](-wia-iwiadispatchitem-takepicture.md) del objeto de **elemento** hace que un dispositivo de cámara digital tome una imagen y devuelve un objeto de **elemento** que representa la imagen resultante. Este método solo se aplica a los dispositivos de cámara digital.<br/> |
| [**Transferencia**](-wia-iwiadispatchitem-transfer.md)             | El método [**Transfer**](-wia-iwiadispatchitem-transfer.md) del objeto **Item** transfiere datos de un dispositivo a un archivo. Este método solo se aplica a los elementos de tipo de dispositivo.<br/>                                                                                         |



 

### <a name="properties"></a>Propiedades

El objeto de **elemento** tiene estas propiedades.



| Propiedad                                                                    | Tipo de acceso          | Descripción                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Solo lectura<br/> | La propiedad [**Children**](-wia-iwiadispatchitem-children.md) del objeto **Item** recupera una colección de objetos **Item** . Los elementos de esta colección representan elementos que son elementos secundarios directos de este elemento en el árbol jerárquico. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Solo lectura<br/> | Recupera el estado de conexión del dispositivo. Esta propiedad solo se aplica a los elementos de tipo Device (elementos raíz). Los valores posibles son "conectado", "desconectado" o **null** (si esta propiedad no se aplica al elemento). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Solo lectura<br/> | Recupera la versión de firmware del dispositivo. Esta propiedad solo se aplica a los elementos de tipo Device (elementos raíz). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Solo lectura<br/> | Recupera el nombre completo del elemento tal y como aparece en la interfaz de usuario. <br/>                                                                                                                                                                                    |
| [**Height**](-wia-iwiadispatchitem-height.md)<br/>                   | Solo lectura<br/> | Alto, en píxeles, del elemento. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Solo lectura<br/> | Tipo de este elemento. <br/>                                                                                                                                                                                                                          |
| [**Name**](-wia-iwiadispatchitem-name.md)<br/>                       | Solo lectura<br/> | Nombre del elemento tal y como aparece en la interfaz de usuario. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Solo lectura<br/> | Alto, en píxeles, de las imágenes generadas por esta cámara digital. Solo se aplica a cámaras digitales. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Solo lectura<br/> | Ancho, en píxeles, de las imágenes generadas por esta cámara digital. Solo se aplica a cámaras digitales. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Solo lectura<br/> | Alto, en píxeles, de la imagen en miniatura. Esta propiedad devuelve-1 si este elemento no admite miniaturas. <br/>                                                                                                                               |
| [**Miniatura**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Solo lectura<br/> | Ruta de acceso y nombre de archivo de la imagen en miniatura. Esta propiedad es **null** si el elemento no admite vistas en miniatura o si no se puede compilar una ruta de acceso. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Solo lectura<br/> | Ancho, en píxeles, de la imagen en miniatura. Esta propiedad devuelve-1 si este elemento no admite miniaturas. <br/>                                                                                                                                |
| [**Tiempo**](-wia-iwiadispatchitem-time.md)<br/>                       | Solo lectura<br/> | La hora actual. Solo se aplica a dispositivos. <br/>                                                                                                                                                                                                      |
| [**Width**](-wia-iwiadispatchitem-width.md)<br/>                     | Solo lectura<br/> | Ancho, en píxeles, del elemento. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Observaciones

### <a name="creationaccess-functions"></a>Funciones de acceso de creación \\

Use cualquiera de las siguientes opciones para recuperar una referencia al objeto:



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**A**](-wia-iwiadeviceinfo-create.md)

[**Crear**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




