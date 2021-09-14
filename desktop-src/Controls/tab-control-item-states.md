---
title: Estados de elemento de control tab (CommCtrl.h)
description: Los elementos de control de tabulación ahora admiten un estado de elemento para admitir el mensaje \_ TCM DESELECTALL. Además, la estructura TCITEM admite valores de estado de elemento.
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
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166938"
---
# <a name="tab-control-item-states"></a>Estados de los elementos de control tab

Los elementos de control de tabulación ahora admiten un estado de elemento para admitir el [**mensaje \_ TCM DESELECTALL.**](tcm-deselectall.md) Además, la estructura [**TCITEM admite**](/windows/win32/api/commctrl/ns-commctrl-tcitema) valores de estado de elemento.



| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [Versión 4.70.](common-control-versions.md) El elemento de control de pestaña está seleccionado. Este estado solo es significativo si se ha [**establecido la marca de estilo \_ TCS BUTTONS.**](tab-control-styles.md)<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ RESALTADO**</dt> </dl>       | [Versión 4.71.](common-control-versions.md) El elemento de control de tabulación está resaltado y la pestaña y el texto se dibujan con el color de resaltado actual. Cuando se usa un color alto, será una interpolación verdadera, no un color entrelazado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





