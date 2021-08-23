---
description: Códigos de error específicos de XAudio2 devueltos por métodos XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Códigos de error de XAudio2 (Xaudio2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bbfb29153ca55064c1019e9cfb8fd1019caaa0ffe17dfa103f123faa812f762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545405"
---
# <a name="xaudio2-error-codes"></a>Códigos de error de XAudio2

Códigos de error específicos de XAudio2 devueltos por métodos XAudio2.



| Constante o valor                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <dt>**XAUDIO2 \_ E \_ NOMBRE DE \_ LLAMADA**</dt> <dt>NO 0X88960001</dt> </dl>                          | XAudio2 devuelve ciertos errores de uso de API (llamadas no válidas, entre otros) que son difíciles de evitar por completo y deben controlarse mediante un título en tiempo de ejecución. (Los errores de uso de API que son completamente evitables, como parámetros no válidos, provocan una aserción en las compilaciones de depuración y un comportamiento indefinido en las compilaciones comerciales, por lo que no se define ningún código de error para ellas).<br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <dt>**XAUDIO2 \_ E \_ ERROR DEL \_ DESCODIFICADOR \_ XMA**</dt> <dt>0x88960002</dt> </dl>          | El Xbox 360 hardware XMA produjo un error irrecuperable.<br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <dt>**XAUDIO2 \_ E ERROR \_ DE CREACIÓN \_ DE \_ XAPO**</dt> <dt>0x88960003</dt> </dl> | No se pudo crear una instancia de un efecto.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <dt>**XAUDIO2 \_ E \_ DEVICE \_ INVALIDTED**</dt> <dt>0x88960004</dt> </dl>        | Un dispositivo de audio se hizo inutilizable al desconectarse o algún otro evento.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Comentarios

### <a name="platform-requirements"></a>Requisitos de la plataforma

Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); SDK de DirectX (XAudio 2.7)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Xaudio2.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[XAudio2::Constants](constants.md)
</dt> </dl>

 

 




