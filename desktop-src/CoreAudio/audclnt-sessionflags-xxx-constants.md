---
description: Las constantes AUDCLNT \_ SESSIONFLAGS XXX indican las características de una sesión de audio asociada a la \_ secuencia.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: AUDCLNT_SESSIONFLAGS_XXX constantes (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165162"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>Constantes XXX de AUDCLNT \_ \_ SESSIONFLAGS

Las constantes AUDCLNT \_ SESSIONFLAGS XXX indican las características de una sesión de audio asociada a la \_ secuencia. Un cliente puede especificar estas opciones durante la inicialización de la secuencia mediante el parámetro *StreamFlags* del [**método IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)



| Constante o valor                                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ LAS SESSIONFLAGS \_ EXPIRANCUANDO 0X10000000**</dt> <dt></dt> </dl>                       | La sesión expira cuando no hay secuencias asociadas y posee objetos de control de sesión que mantienen referencias.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ PANTALLA SESSIONFLAGS \_ \_ HIDE**</dt> <dt>0x20000000</dt> </dl>                                     | El control de volumen está oculto en la interfaz de usuario del mezclador de volúmenes cuando se crea la sesión de audio. Si la sesión asociada a la secuencia ya existe antes de [**que IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) abra la secuencia, el control de volumen se muestra en el mezclador de volúmenes.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **LAS SESSIONFLAGS DE AUDCLNT \_ \_ MUESTRAN \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | El control de volumen se oculta en la interfaz de usuario del mezclador de volúmenes después de que expire la sesión. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




