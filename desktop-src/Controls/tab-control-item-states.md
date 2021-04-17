---
title: Estados de elemento de control de pestaña (CommCtrl. h)
description: Los elementos de control de pestaña ahora admiten un estado de elemento para admitir el \_ mensaje DESELECTALL de TCM. Además, la estructura TCITEM admite valores de estado del elemento.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660471"
---
# <a name="tab-control-item-states"></a>Estados de elemento de control de pestaña

Los elementos de control de pestaña ahora admiten un estado de elemento para admitir el mensaje [**\_ DESELECTALL de TCM**](tcm-deselectall.md) . Además, la estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) admite valores de estado del elemento.



| Constante                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**TCIS \_ BUTTONPRESSED**</dt> </dl> | [Versión 4,70](common-control-versions.md). Se selecciona el elemento de control de pestaña. Este estado solo es significativo si se ha establecido la marca de estilo [**\_ botones de TCS**](tab-control-styles.md) .<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ resaltado**</dt> </dl>       | [Versión 4,71](common-control-versions.md). Se resalta el elemento de control de pestaña y la pestaña y el texto se dibujan con el color de resaltado actual. Cuando se usa el color de alta densidad, se trata de una interpolación verdadera, no de un color interpolado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





