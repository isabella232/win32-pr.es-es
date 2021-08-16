---
title: Valores de dibujo personalizados (CommCtrl.h)
description: En esta sección se enumeran los valores usados para identificar las partes de un control Trackbar.
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
ms.openlocfilehash: cb714df7c91819a7d459c4c9fbed1fbc1e0d4fd2455f52891030d95991fa6497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831696"
---
# <a name="custom-draw-values"></a>Valores de dibujo personalizados

En esta sección se enumeran los valores usados para identificar las partes de un control Trackbar.



| Constante                                                                                                                                                   | Descripción                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**CANAL \_ TBCD**</dt> </dl> | Identifica el canal en el que se desliza el marcador de posición del control de la barra de seguimiento.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifica el marcador de posición del control trackbar. Esta es la parte del control que mueve el usuario.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica las marcas de graduación que se muestran a lo largo del borde del control de barra de seguimiento.<br/>                      |



## <a name="remarks"></a>Comentarios

Los valores draw personalizados, por ejemplo, se especifican en el **miembro dwItemSpec** de la [**estructura NMCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





