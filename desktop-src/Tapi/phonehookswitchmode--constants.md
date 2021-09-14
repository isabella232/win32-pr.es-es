---
description: Las constantes de marca de bits PHONEHOOKSWITCHMODE describen los componentes de micrófono y \_ altavoz de un dispositivo de conmutador de enlace.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: PHONEHOOKSWITCHMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068732"
---
# <a name="phonehookswitchmode_-constants"></a>Constantes PHONEHOOKSWITCHMODE \_

Las constantes de marca de bits **PHONEHOOKSWITCHMODE \_** describen los componentes de micrófono y altavoz de un dispositivo de conmutador de enlace.

<dl> <dt>

<span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE \_ MIC**
</dt> <dd> <dl> <dt>



El micrófono del dispositivo está activo, el altavoz se silencia.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**
</dt> <dd> <dl> <dt>



El micrófono y el altavoz del dispositivo están activos.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE \_ ONHOOK**
</dt> <dd> <dl> <dt>



El micrófono y el altavoz del dispositivo son ambos onhook.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ SPEAKER**
</dt> <dd> <dl> <dt>



El altavoz del dispositivo está activo, el micrófono se silencia.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Actualmente se desconoce el modo de conmutador de enlace del dispositivo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

Estas constantes se usan para proporcionar un nivel individual de control sobre los componentes de micrófono y altavoz de un dispositivo telefónico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




