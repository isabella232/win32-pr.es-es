---
description: Los GUID de la clase terminal identifican un terminal determinado por funcionalidades.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Clase terminal (Tapi3if.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd20d3e540529b343d1fb848b9e8cb2579a621b40146e0d170fdb175c4c9a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975455"
---
# <a name="terminal-class"></a>Terminal (clase)

Los GUID de la clase terminal identifican un terminal determinado por funcionalidades.

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



Teléfono.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID \_ HeadsetTerminal**
</dt> <dd> <dl> <dt>



Conjunto principal.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



Terminal de secuencia multimedia, creado dinámicamente.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID \_ MicrophoneTerminal**
</dt> <dd> <dl> <dt>



Micrófono.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



Teléfono del hablante.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**Altavoces \_ CLSIDTerminal**
</dt> <dd> <dl> <dt>



Altavoces.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



Terminal de entrada de vídeo.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ VideoWindowTerm**
</dt> <dd> <dl> <dt>



Ventana de visualización de vídeo, creada dinámicamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

La **versión BSTR** de las clases de terminal se designa principalmente para el uso de Visual Basic aplicaciones. (Por ejemplo, se devuelven como los elementos de la colección obtenidos con [**get \_ DynamicTerminalClasses).**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses)

-   BSTR CLSID \_ String \_ HandsetTerminal
-   BSTR CLSID \_ String \_ HeadsetTerminal
-   Cadena BSTR CLSID \_ \_ MediaStreamTerminal
-   BSTR CLSID \_ String \_ MicrophoneTerminal
-   BSTR CLSID \_ String \_ SpeakerphoneTerminal
-   BSTR CLSID \_ String \_ SpeakersTerminal
-   BSTR CLSID \_ String \_ VideoInputTerminal
-   BSTR CLSID \_ String \_ VideoWindowTerm

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Header<br/>       | <dl> <dt>Tapi3if.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

