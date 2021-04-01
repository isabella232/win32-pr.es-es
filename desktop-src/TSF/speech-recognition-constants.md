---
title: Constantes de reconocimiento de voz (Ctffunc. h)
description: Los siguientes valores se usan con el servicio de texto de reconocimiento de voz.
ms.assetid: ac433d15-738a-46ab-8f69-0fbfb6a8b654
topic_type:
- apiref
api_name:
- TF_DICTATION_ON
- TF_DICTATION_ENABLED
- TF_COMMANDING_ENABLED
- TF_COMMANDING_ON
- TF_SPEECHUI_SHOWN
- TF_SHOW_BALLOON
- TF_DISABLE_BALLOON
- TF_DISABLE_SPEECH
- TF_DISABLE_DICTATION
- TF_DISABLE_COMMANDING
api_location:
- Ctffunc.h
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04c9cfd340e79415d12202765a8db1578abba74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149961"
---
# <a name="speech-recognition-constants"></a>Constantes de reconocimiento de voz

Los siguientes valores se usan con el servicio de texto de reconocimiento de voz.



| Constante o valor                                                                                                                                                                                                                                         | Descripción                                                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DICTATION_ON"></span><span id="tf_dictation_on"></span><dl> <dt>**TF \_ DICTAdo \_ en**</dt> <dt>0x00000001</dt> </dl>                   | Si este bit es 1, el dictado de voz está activo. De lo contrario, el dictado de voz está inactivo. Este valor no se puede combinar con el \_ comando TF \_ activado. Se usa con el compartimiento de [DICTATIONSTAT de voz de compartimiento de GUID \_ \_ \_ ](predefined-compartments.md) .<br/> |
| <span id="TF_DICTATION_ENABLED"></span><span id="tf_dictation_enabled"></span><dl> <dt>**TF \_ DICTAdo \_ habilitado**</dt> <dt>0x00000002</dt> </dl>    | Si este bit es 1, el dictado de voz está habilitado. De lo contrario, el dictado de voz está deshabilitado. Se usa con el compartimiento de [DICTATIONSTAT de voz de compartimiento de GUID \_ \_ \_ ](predefined-compartments.md) .<br/>                                                       |
| <span id="TF_COMMANDING_ENABLED"></span><span id="tf_commanding_enabled"></span><dl> <dt>**TF \_ COMANDO \_ habilitado**</dt> <dt>0x00000004</dt> </dl> | Si este bit es 1, el comando de voz está habilitado. De lo contrario, el comando de voz está deshabilitado. Se usa con el compartimiento de [DICTATIONSTAT de voz de compartimiento de GUID \_ \_ \_ ](predefined-compartments.md) .<br/>                                                           |
| <span id="TF_COMMANDING_ON"></span><span id="tf_commanding_on"></span><dl> <dt>**TF \_ COMANDO \_ en**</dt> <dt>0x00000008</dt> </dl>                | Si este bit es 1, el comando de voz está activo. De lo contrario, el comando de voz está inactivo. Este valor no se puede combinar con el \_ dictado TF \_ en. Se usa con el compartimiento de [DICTATIONSTAT de voz de compartimiento de GUID \_ \_ \_ ](predefined-compartments.md) .<br/>      |
| <span id="TF_SPEECHUI_SHOWN"></span><span id="tf_speechui_shown"></span><dl> <dt>**TF \_ SPEECHUI \_ muestra**</dt> <dt>0x00000010</dt> </dl>             | No se usa actualmente.<br/>                                                                                                                                                                                                                              |
| <span id="TF_SHOW_BALLOON"></span><span id="tf_show_balloon"></span><dl> <dt>**TF \_ Mostrar \_ globo**</dt> <dt>0x00000001</dt> </dl>                   | No se usa actualmente. Se usa con el compartimiento de [Estado de UI de Speech de compartimiento de GUID \_ \_ \_ \_ ](predefined-compartments.md) .<br/>                                                                                                                              |
| <span id="TF_DISABLE_BALLOON"></span><span id="tf_disable_balloon"></span><dl> <dt>**TF \_ Deshabilitar el \_ globo**</dt> <dt>0x00000002</dt> </dl>          | Si este bit es 1, la presentación de globos para el modo de voz actual está deshabilitada. De lo contrario, se habilita la presentación de globo para el modo de voz actual. Se usa con el compartimiento de [Estado de UI de Speech de compartimiento de GUID \_ \_ \_ \_ ](predefined-compartments.md) .<br/>    |
| <span id="TF_DISABLE_SPEECH"></span><span id="tf_disable_speech"></span><dl> <dt>**TF \_ Deshabilitar \_ voz**</dt> <dt>0x00000001</dt> </dl>             | Si este bit es 1, la entrada de voz está deshabilitada. De lo contrario, la entrada de voz está habilitada. Se usa con el compartimiento [ \_ \_ \_ deshabilitado de voz de compartimiento de GUID](predefined-compartments.md) .<br/>                                                                    |
| <span id="TF_DISABLE_DICTATION"></span><span id="tf_disable_dictation"></span><dl> <dt>**TF \_ Deshabilitar \_ dictado**</dt> <dt>0x00000002</dt> </dl>    | Si este bit es 1, el dictado de voz está deshabilitado. De lo contrario, el dictado de voz está habilitado. Se usa con el compartimiento [ \_ \_ \_ deshabilitado de voz de compartimiento de GUID](predefined-compartments.md) .<br/>                                                            |
| <span id="TF_DISABLE_COMMANDING"></span><span id="tf_disable_commanding"></span><dl> <dt>**TF \_ Deshabilitar \_ comandos**</dt> <dt>0x00000004</dt> </dl> | Si este bit es 1, el comando de voz está deshabilitado. De lo contrario, el comando de voz está habilitado. Se usa con el compartimiento [ \_ \_ \_ deshabilitado de voz de compartimiento de GUID](predefined-compartments.md) .<br/>                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                    |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                                                                                         |
| Encabezado<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Msctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compartimientos predefinidos](predefined-compartments.md)
</dt> </dl>

 

 





