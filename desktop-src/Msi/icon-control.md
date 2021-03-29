---
description: El control de icono muestra una imagen estática de un icono. El fondo de la imagen es transparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Control de icono (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a9bf90697ff3a839c1953918179fb8cf41f2809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540251"
---
# <a name="icon-control"></a>Control de icono

El control de icono muestra una imagen estática de un icono. El fondo de la imagen es transparente.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con este control. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                         | Bit hexadecimal                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Texto](text-control-attribute.md)           |                                                                              | Contiene el nombre de un icono almacenado en la [tabla binaria](binary-table.md). Para mostrar un icono que está almacenado en la tabla binaria, escriba el nombre del registro de la imagen que aparece en la tabla binaria en la columna texto del registro de la [tabla de control](control-table.md) para este control.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md) para que el control sea visible u oculto en el momento de su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Muestra el estilo visual predeterminado. Muestra el control con una apariencia en relieve y 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Estira la imagen del icono para ajustarse al control. Recorta o centra la imagen de icono en el control.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Iconos](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Carga la primera imagen. Carga la primera imagen de 16x16.<br/> Carga la primera imagen 32x32.<br/> Carga la primera imagen de 48x48.<br/> Un archivo de icono puede contener imágenes de tamaño diferentes del mismo icono. Incluya el valor de la palabra de bit adecuada en la columna Attributes de la [tabla de control](control-table.md) .<br/> Si no se establecen estos bits, el instalador omite el atributo FixedSize y la imagen se ajusta para ajustarse al rectángulo de control. Si se establecen los dos iconos de los bits y los bits FixedSize, se centra una imagen menor que el control y una imagen es mayor que el control que se reduce para ajustarse.<br/> |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase estática mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos **SS \_ Icon**, **SS \_ CENTERIMAGE**, **WS \_ Child** y **WS \_ Group** .

 

 
