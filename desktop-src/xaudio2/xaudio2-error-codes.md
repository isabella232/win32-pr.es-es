---
description: Códigos de error específicos de XAudio2 devueltos por los métodos de XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Códigos de error de XAudio2 (xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700184"
---
# <a name="xaudio2-error-codes"></a>Códigos de error de XAudio2

Códigos de error específicos de XAudio2 devueltos por los métodos de XAudio2.



| Constante o valor                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ \_ llamada no válida**</dt> <dt>0x88960001</dt> </dl>                          | Lo devuelve XAudio2 para ciertos errores de uso de la API (llamadas no válidas, etc.) que son difíciles de evitar completamente y deben controlarse mediante un título en tiempo de ejecución. (Los errores de uso de la API que son completamente evitables, como los parámetros no válidos, causan una ASERCIÓN en las compilaciones de depuración y el comportamiento indefinido en las compilaciones comerciales, por lo que no se define ningún código de error para ellos)<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ E \_ XMA \_ \_ error del descodificador**</dt> <dt>0x88960002</dt> </dl>          | Se produjo un error irrecuperable en el hardware de XMA de Xbox 360.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ \_ \_ \_ Error**</dt> en la creación de XAPO <dt>0x88960003</dt> </dl> | No se pudo crear una instancia de un efecto.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ \_Dispositivo E \_ invalidado**</dt> <dt>0x88960004</dt> </dl>        | Un dispositivo de audio dejó de ser utilizable a través de desenchufado o algún otro evento.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Observaciones

### <a name="platform-requirements"></a>Requisitos de la plataforma

Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK de DirectX (XAudio 2,7)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Xaudio2. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[XAudio2:: constantes](constants.md)
</dt> </dl>

 

 




