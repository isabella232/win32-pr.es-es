---
description: Los GUID de clase de terminal identifican un terminal determinado por capacidades.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Clase terminal (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d67d7668f9e4e16ad357408c8e9087fce870a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680930"
---
# <a name="terminal-class"></a>Clase terminal

Los GUID de clase de terminal identifican un terminal determinado por capacidades.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**CLSID \_ FilePlaybackTerminal**
</dt> <dd> <dl> <dt>



Terminal de reproducción de archivos.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**CLSID \_ FileRecordingTerminal**
</dt> <dd> <dl> <dt>



Terminal de grabación de archivos.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**CLSID \_ FileRecordingTrack**
</dt> <dd> <dl> <dt>



Pista de grabación de archivos.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**CLSID \_ HandsetTerminal**
</dt> <dd> <dl> <dt>



Auricular del teléfono.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID \_ HeadsetTerminal**
</dt> <dd> <dl> <dt>



Conjunto principal.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



Terminal de flujo de medios, creado dinámicamente.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID \_ MicrophoneTerminal**
</dt> <dd> <dl> <dt>



Micrófono.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



Altavoz teléfono.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**CLSID \_ SpeakersTerminal**
</dt> <dd> <dl> <dt>



Participantes.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



Terminal de entrada de vídeo.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ VideoWindowTerm**
</dt> <dd> <dl> <dt>



Ventana de presentación de vídeo, creada dinámicamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

La versión **BSTR** de las clases terminal se designa principalmente para el uso de aplicaciones Visual Basic. (Por ejemplo, se devuelven como los elementos de la colección obtenida con [**Get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)).

-   BSTR CLSID \_ String \_ HandsetTerminal
-   BSTR CLSID \_ String \_ HeadsetTerminal
-   BSTR CLSID \_ String \_ MediaStreamTerminal
-   BSTR CLSID \_ String \_ MicrophoneTerminal
-   BSTR CLSID \_ String \_ SpeakerphoneTerminal
-   BSTR CLSID \_ String \_ SpeakersTerminal
-   BSTR CLSID \_ String \_ VideoInputTerminal
-   BSTR CLSID \_ String \_ VideoWindowTerm

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal:: get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

