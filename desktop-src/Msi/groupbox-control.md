---
description: El control GroupBox muestra un rectángulo, posiblemente con texto de título, que sirve para agrupar otros controles en el cuadro de diálogo.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: Control GroupBox (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275926"
---
# <a name="groupbox-control"></a>Control GroupBox

El control GroupBox muestra un rectángulo, posiblemente con texto de título, que sirve para agrupar otros controles en el cuadro de diálogo.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con el control GroupBox. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la tabla de [control](control-table.md) o de la [tabla BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                                                                                                         |
| [Texto](text-control-attribute.md)                 |                                  | Muestra un título en la esquina superior izquierda del control. Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&Style}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Attributes de la tabla de [control](control-table.md) o la [tabla BBControl](bbcontrol-table.md) para que el control esté visible u oculto en su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con una apariencia en relieve y 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control está alineado a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase BUTTON mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Tiene los estilos de grupo **\_ GROUPBOX**, **WS \_ secundario** y **WS \_ Group** .

Siempre hay un hueco entre la parte superior de la ventana del control y el marco visible, incluso cuando no hay ningún título.

 

 
