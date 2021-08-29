---
description: El control Línea es una línea horizontal.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Control de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763495"
---
# <a name="line-control"></a>Control de línea

El control Línea es una línea horizontal.

## <a name="control-attributes"></a>Atributos de control

Puede usar los atributos siguientes con este control. Para cambiar el valor de un atributo mediante un evento, suscribe el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumera el identificador del atributo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                       | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md) |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la tabla [Control](control-table.md) o [de la tabla BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos en la [tabla Control](control-table.md) o en la tabla [BBControl](bbcontrol-table.md) para que el control sea visible u oculto tras su creación.<br/> También puede ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D a la vista.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentarios

Este control se puede crear a partir de la clase STATIC mediante [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Tiene los **estilos SS \_ ETCHEDHORZ** y **SS \_ SUNKEN.**

 

 
