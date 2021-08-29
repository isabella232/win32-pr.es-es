---
description: Las constantes de marca de bits LINECALLHUBTRACKING describen el tipo de seguimiento del \_ centro de llamadas proporcionado.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: LINECALLHUBTRACKING_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d24b9641e7662871aef64f1358eeddfb58f5c9400b45aee405b8c6d8f134a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405195"
---
# <a name="linecallhubtracking_-constants"></a>Constantes LINECALLHUBTRACKING \_

Las constantes de marca de bits **LINECALLHUBTRACKING \_** describen el tipo de seguimiento del centro de llamadas proporcionado.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**
</dt> <dd> <dl> <dt>



El seguimiento del centro de llamadas se proporciona en el nivel de llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ NONE**
</dt> <dd> <dl> <dt>



No se proporciona ningún seguimiento del centro de llamadas.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**
</dt> <dd> <dl> <dt>



Se realiza un seguimiento de los centros de llamadas en el nivel de proveedor de servicios. No se notifican los cambios de llamada a por llamada.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Cuando se producen cambios en esta estructura de datos, se envía un [**mensaje LINE \_ CALLINFO**](line-callinfo.md) a la aplicación. Los parámetros de este mensaje son un identificador de la llamada y una indicación del elemento de información que ha cambiado. La [**estructura de datos LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica qué tipo de seguimiento se proporciona.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINE \_ CALLINFO**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




