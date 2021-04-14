---
description: Las \_ \_ constantes de AUDCLNT SESSIONFLAGS XXX indican características de una sesión de audio asociada a la secuencia.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Constantes de AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496696"
---
# <a name="audclnt_sessionflags_xxx-constants"></a>Constantes de AUDCLNT \_ SESSIONFLAGS \_ XXX

Las \_ \_ constantes de AUDCLNT SESSIONFLAGS XXX indican características de una sesión de audio asociada a la secuencia. Un cliente puede especificar estas opciones durante la inicialización de la secuencia mediante el parámetro *StreamFlags* del método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .



| Constante o valor                                                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt> </dl>                       | La sesión expira cuando no hay secuencias asociadas y objetos de control de sesión propietarios que contienen referencias.<br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <dt>**AUDCLNT \_ SESSIONFLAGS \_ Mostrar \_ ocultar**</dt> <dt>0x20000000</dt> </dl>                                     | El control de volumen se oculta en la interfaz de usuario del mezclador de volumen cuando se crea la sesión de audio. Si la sesión asociada a la secuencia ya existe antes de que [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Abra el flujo, el control de volumen se mostrará en el mezclador de volumen.<br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <dt> **AUDCLNT \_ SESSIONFLAGS \_ Display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt> </dl> | El control de volumen se oculta en la interfaz de usuario del mezclador de volumen después de que expire la sesión. <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




