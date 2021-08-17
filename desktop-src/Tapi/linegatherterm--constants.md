---
description: Las constantes de marca de bits LINEGATHERTERM describen las condiciones en las que finaliza la recopilación \_ de dígitos almacenados en búfer.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: LINEGATHERTERM_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a6d5952ac4f69d11fd499df63554d6fda7dca76e46e4aad1a01ae326f363a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140038"
---
# <a name="linegatherterm_-constants"></a>LineGATHERTERM \_ (constantes)

Las constantes de marca de bits **LINEGATHERTERM \_** describen las condiciones en las que finaliza la recopilación de dígitos almacenados en búfer.

<dl> <dt>

<span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**
</dt> <dd> <dl> <dt>



Se ha recopilado el número solicitado de dígitos. El búfer está lleno.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ CANCEL**
</dt> <dd> <dl> <dt>



Esta aplicación canceló la solicitud, otra aplicación o porque la llamada finalizó.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**
</dt> <dd> <dl> <dt>



El tiempo de espera del primer dígito expiró. El búfer no contiene dígitos.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM \_ INTERTIMEOUT**
</dt> <dd> <dl> <dt>



El tiempo de espera entre dígitos expiró. El búfer contiene al menos un dígito.


</dt> </dl> </dd> <dt>

<span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**
</dt> <dd> <dl> <dt>



Uno de los dígitos de terminación coincidía con un dígito recibido. El dígito de terminación coincidente es el último dígito del búfer.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




