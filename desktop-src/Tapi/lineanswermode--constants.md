---
description: Las constantes de marca de bits LINEANSWERMODE describen cómo se ve afectada una llamada activa existente en un dispositivo de línea al responder a otra llamada de oferta \_ en la misma línea.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfb9d6491864f5be8788575d718e42cc5f5c7c337fd046c110bd5bd82eae110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761847"
---
# <a name="lineanswermode_-constants"></a>Constantes LINEANSWERMODE \_

Las constantes de marca de bits **LINEANSWERMODE \_** describen cómo se ve  afectada una llamada activa existente en un dispositivo de línea al responder a otra llamada de oferta en la misma línea.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**
</dt> <dd> <dl> <dt>



La llamada activa actualmente se descartará automáticamente.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ HOLD**
</dt> <dd> <dl> <dt>



La llamada activa actualmente se colocará automáticamente en espera.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ NONE**
</dt> <dd> <dl> <dt>



Responder a otra llamada en la misma línea no tiene ningún efecto en la llamada activa existente en la línea.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Si una llamada entra (se ofrece) en el momento en que otra llamada ya está activa, la nueva llamada se conecta invocando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). El efecto que esto tiene en la llamada activa existente depende de las funcionalidades del dispositivo de la línea. La primera llamada puede no resultar afectada, se puede descartar automáticamente o se puede colocar automáticamente en espera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




