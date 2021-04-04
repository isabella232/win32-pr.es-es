---
description: El control de la cartelera muestra los controles que se usan con frecuencia y que se agregan y se quitan del cuadro de diálogo ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Control de cartelera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909066"
---
# <a name="billboard-control"></a>Control de cartelera

El control de la cartelera muestra los controles que se usan con frecuencia y que se agregan y se quitan del cuadro de diálogo ControlEvents. Solo los controles que no están asociados a una propiedad, como [texto](text-control.md), [mapa de bits](bitmap-control.md), [icono](icon-control.md)o controles personalizados, se pueden colocar en una cartelera. Los controles de la cartelera suelen mostrar mensajes de progreso.

## <a name="control-attributes"></a>Atributos de control

Puede usar los siguientes atributos con el control de la cartelera. Para cambiar el valor de un atributo mediante un evento, suscríbase el control a ControlEvent, en la [tabla EventMapping](eventmapping-table.md) y enumere el identificador del atributo en la columna de atributos. Escriba el identificador de ControlEvent, en la columna evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BillboardName](billboardname-control-attribute.md) |                                  | Nombre de la cartelera actual. Escriba el identificador de la cartelera en la columna cartelera de la [tabla BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                            |
| [Position](position-control-attribute.md)           |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas de la esquina izquierda del control en las columnas width, height, X e Y de la [tabla BBControl](bbcontrol-table.md). Use [unidades de instalador](installer-units.md) para longitud y distancia.<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bit de la columna Attributes de la [tabla BBControl](bbcontrol-table.md) para que el control esté visible u oculto en su creación.<br/> Ocultar o mostrar un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto hundido, 3D.<br/> Incluya estos bits en la palabra de bit de la columna Attributes de la [tabla de control](control-table.md).<br/>                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Este control no tiene ninguna ventana propia.

Los controles de la cartelera que aparecen en la interfaz de usuario completa se enumeran en la tabla de la [cartelera](billboard-table.md).

Los controles que se encuentran en una cartelera deben aparecer en la [tabla BBControl](bbcontrol-table.md) en lugar de en la [tabla de control](control-table.md).

 

 




