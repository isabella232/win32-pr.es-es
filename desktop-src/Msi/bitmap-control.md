---
description: El control Bitmap muestra un archivo de imagen estática JPEG o de mapa de bits. El Windows instalador determinará automáticamente el formato de los datos binarios y mostrará la imagen. El control no admite la animación.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Control de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158969"
---
# <a name="bitmap-control"></a>Control de mapa de bits

El control Bitmap muestra un archivo de imagen estática JPEG o de mapa de bits. El Windows instalador determinará automáticamente el formato de los datos binarios y mostrará la imagen. El control no admite la animación.

**Windows 8 y Windows Server 2012:** El archivo de imagen puede estar en cualquier formato estándar compatible con Windows Imaging Component (WIC), incluido TIFF, JPEG, PNG, GIF, BMP y HDPhoto. El control no admite la animación.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, alto y coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la tabla [Control](control-table.md) o [BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                         |
| [Texto](text-control-attribute.md)                   |                                  | Contiene el nombre de un mapa de bits almacenado en la [tabla binaria](binary-table.md). Para mostrar un mapa de bits almacenado en la tabla Binary, haga lo siguiente. Escriba el nombre de la imagen de mapa de bits que aparece en la columna Nombre de la tabla Binaria en la columna Texto del registro de tabla [Control](control-table.md) de este control. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md) o de la tabla [BBControl](bbcontrol-table.md)para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                   |
| [FixedSize (control)](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Ajusta la imagen de mapa de bits para ajustarla al control. Recorta o centra la imagen de mapa de bits en el control .<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla BBControl](bbcontrol-table.md) o [de la tabla Control](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase STATIC mediante [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos **SS \_ BITMAP**, **SS \_ CENTERIMAGE,** **WS \_ CHILD** y **WS \_ GROUP.**

 

