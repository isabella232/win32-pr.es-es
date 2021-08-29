---
description: El control Deón muestra los controles usados habitualmente que ControlEvents agrega y quita del cuadro de diálogo.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Control Descontrol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5671cd9f345bb4a93efb0a103017fe733bf35beaf58d271c1c2e9906daa9ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105405"
---
# <a name="billboard-control"></a>Control Descontrol

El control Deón muestra los controles usados habitualmente que ControlEvents agrega y quita del cuadro de diálogo. Solo los controles que no están asociados a una propiedad, como [Texto,](text-control.md)Mapa de [bits](bitmap-control.md)o [Icono,](icon-control.md)o los controles personalizados se pueden colocar en una barra. Los controles Deserción suelen mostrar mensajes de progreso.

## <a name="control-attributes"></a>Atributos de control

Puede usar los atributos siguientes con el control Dedón. Para cambiar el valor de un atributo mediante un evento, suscribe el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md) y enumera el identificador del atributo en la columna Atributo . Escriba el identificador de ControlEvent en la columna Evento.



| Identificador de atributo                                 | Bit hexadecimal                  | Descripción                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NameName](billboardname-control-attribute.md) |                                  | Nombre de la lista actual. Escriba el identificador de la cadena en la columna De la tabla [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                            |
| [Position](position-control-attribute.md)           |                                  | Posición del control en el cuadro de diálogo. Escriba el ancho, el alto y las coordenadas del control de la esquina izquierda del control en las columnas Width, Height, X e Y de la [tabla BBControl](bbcontrol-table.md). Use [las unidades del](installer-units.md) instalador para la longitud y la distancia.<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Control oculto. Control visible.<br/> Incluya este bit en la palabra de bits de la columna Atributos de la tabla [BBControl](bbcontrol-table.md) para que el control sea visible u oculto tras su creación.<br/> Oculte o muestre un control mediante la [tabla ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Muestra el estilo visual predeterminado. Muestra el control con un aspecto 3D.<br/> Incluya estos bits en la palabra de bits en la columna Atributos de la [tabla Control](control-table.md).<br/>                                                                                                               |



 

## <a name="remarks"></a>Comentarios

Este control no tiene ninguna ventana propia.

Los controles de la lista de paneles que aparecen en la interfaz de usuario completa se muestran en la [tabla Deserción.](billboard-table.md)

Los controles que se encuentran en un tablero deben aparecer en la [tabla BBControl](bbcontrol-table.md) en lugar de en [la tabla Control](control-table.md).

 

 




