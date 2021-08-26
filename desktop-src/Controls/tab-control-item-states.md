---
title: Estados del elemento de control Tab (CommCtrl.h)
description: Los elementos de control tab ahora admiten un estado de elemento para admitir el mensaje \_ TCM DESELECTALL. Además, la estructura TCITEM admite valores de estado de elemento.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75f3bba0ecd29c7ab84c6b68010f8af52c8db2cfc9dc4080fb73e37b408ee1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919285"
---
# <a name="tab-control-item-states"></a>Estados del elemento de control Tab

Los elementos de control tab ahora admiten un estado de elemento para admitir el [**mensaje \_ TCM DESELECTALL.**](tcm-deselectall.md) Además, la estructura [**TCITEM admite**](/windows/win32/api/commctrl/ns-commctrl-tcitema) valores de estado de elemento.



| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [Versión 4.70.](common-control-versions.md) El elemento de control de pestaña está seleccionado. Este estado solo es significativo si se ha establecido la marca de [**estilo \_ TCS BUTTONS.**](tab-control-styles.md)<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ RESALTADO**</dt> </dl>       | [Versión 4.71.](common-control-versions.md) El elemento de control de pestaña está resaltado y la pestaña y el texto se dibujan con el color de resaltado actual. Cuando se usa un color alto, será una interpolación verdadera, no un color de trama.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





