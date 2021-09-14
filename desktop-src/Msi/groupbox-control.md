---
description: El control GroupBox muestra un rectángulo, posiblemente con texto de título, que sirve para agrupar otros controles en el cuadro de diálogo.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: Control GroupBox (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074725"
---
# <a name="groupbox-control"></a>Control GroupBox

El control GroupBox muestra un rectángulo, posiblemente con texto de título, que sirve para agrupar otros controles en el cuadro de diálogo.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con el control GroupBox. Para cambiar el valor de un atributo mediante un evento, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumézcalo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                               | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, alto y coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la tabla [Control](control-table.md) o [BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                                                                                                         |
| [Texto](text-control-attribute.md)                 |                                  | Muestra un título en la esquina superior izquierda del control. Para establecer la fuente y el estilo de fuente de una cadena de texto, antefise la cadena de caracteres mostrados con { style} o \\ {&style}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos en la [tabla Control](control-table.md) o en la tabla [BBControl](bbcontrol-table.md) para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/>                                                                             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D desconsolado.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | El texto del control se muestra en orden de lectura de izquierda a derecha. El texto del control se muestra en orden de lectura de derecha a izquierda.<br/>                                                                                                                                                                                                                                                                                                                |
| [Alineado a la derecha](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | El texto del control se alinea a la izquierda. El texto del control se alinea a la derecha.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Observaciones

Este control se puede crear a partir de la clase BUTTON mediante [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los **estilos \_ BS GROUPBOX,** **WS \_ CHILD** y **WS \_ GROUP.**

Siempre hay un intervalo entre la parte superior de la ventana del control y el marco visible, incluso cuando no hay ningún título.

 

 
