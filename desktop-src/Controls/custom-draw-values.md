---
title: Valores de dibujo personalizados (CommCtrl. h)
description: En esta sección se enumeran los valores que se usan para identificar las partes de un control TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649723"
---
# <a name="custom-draw-values"></a>Valores de dibujo personalizados

En esta sección se enumeran los valores que se usan para identificar las partes de un control TrackBar.



| Constante                                                                                                                                                   | Descripción                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifica el canal en el que se desplaza el marcador de control de la barra de desplazamiento.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**\_Thumb TBCD**</dt> </dl>       | Identifica el marcador de control de la barra de desplazamiento. Esta es la parte del control que mueve el usuario.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ las marcas**</dt> </dl>          | Identifica las marcas de graduación que se muestran a lo largo del borde del control TrackBar.<br/>                      |



## <a name="remarks"></a>Observaciones

Los valores de dibujo personalizados, por ejemplo, se especifican en el miembro **dwItemSpec** de la estructura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





