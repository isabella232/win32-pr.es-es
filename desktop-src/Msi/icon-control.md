---
description: El control Icono muestra una imagen estática de un icono. El fondo de la imagen es transparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Control icono (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce6d1dca9e6664018a0c7a36c9b44f3b5a0b6310bc8c6d18309b73649fa9240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996715"
---
# <a name="icon-control"></a>Control icono

El control Icono muestra una imagen estática de un icono. El fondo de la imagen es transparente.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Attribute . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                         | Bit hexadecimal                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas del control de la esquina izquierda del control en las columnas Ancho, Alto, X e Y de la [tabla Control](control-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Texto](text-control-attribute.md)           |                                                                              | Contiene el nombre de un icono almacenado en la [tabla binaria](binary-table.md). Para mostrar un icono almacenado en la tabla Binaria, escriba el nombre del registro de la imagen que aparece en la tabla Binary en la columna Texto del registro de tabla [control](control-table.md) de este control.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md) para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Ajusta la imagen de icono para ajustarla al control. Recorta o centra la imagen de icono en el control.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [IconSize](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Carga la primera imagen. Carga la primera imagen de 16 x 16.<br/> Carga la primera imagen de 32 x 32.<br/> Carga la primera imagen de 48 x 48.<br/> Un archivo de icono puede contener imágenes de tamaño diferente del mismo icono. Incluya el valor de la palabra de bits adecuada en la columna Atributos de la [tabla Control.](control-table.md)<br/> Si no se establecen estos bits, el instalador omite el atributo FixedSize y la imagen se ajusta para ajustarse al rectángulo de control. Si se establecen los bits IconSize y FixedSize, se centra una imagen más pequeña que el control y una imagen es mayor que el control que se va a reducir para ajustarse.<br/> |



 

## <a name="remarks"></a>Comentarios

Este control se puede crear a partir de la clase STATIC mediante [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los estilos **SS \_ ICON**, **SS \_ CENTERIMAGE,** **WS \_ CHILD** y **WS \_ GROUP.**

 

 
