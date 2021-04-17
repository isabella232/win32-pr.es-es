---
description: El control Bitmap muestra un mapa de bits o un archivo de imagen estática JPEG. El Windows Installer determinará automáticamente el formato de los datos binarios y mostrará la imagen. El control no admite la animación.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Control Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667014"
---
# <a name="bitmap-control"></a>Control Bitmap

El control Bitmap muestra un mapa de bits o un archivo de imagen estática JPEG. El Windows Installer determinará automáticamente el formato de los datos binarios y mostrará la imagen. El control no admite la animación.

**Windows 8 y Windows Server 2012:** El archivo de imagen puede estar en cualquier formato estándar compatible con el componente de creación de imágenes de Windows (WIC), incluidos TIFF, JPEG, PNG, GIF, BMP y HDPhoto. El control no admite la animación.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                         |
| [Texto](text-control-attribute.md)                   |                                  | Contiene el nombre de un mapa de bits almacenado en la [tabla binaria](binary-table.md). Para mostrar un mapa de bits almacenado en la tabla binaria, haga lo siguiente. Escriba el nombre de la imagen de mapa de bits que aparece en la columna Nombre de la tabla binaria en la columna texto del registro de la [tabla de control](control-table.md) para este control. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bit de la columna Attributes de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). para hacer que el control esté visible u oculto en su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con una apariencia en relieve y 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                   |
| [Control FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Estira la imagen de mapa de bits para ajustarse al control. Recorta o centra la imagen de mapa de bits en el control.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla BBControl](bbcontrol-table.md) o de la [tabla de control](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase estática mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos **SS \_ Bitmap**, **SS \_ CENTERIMAGE**, **WS \_ Child** y **WS \_ Group** .

 

