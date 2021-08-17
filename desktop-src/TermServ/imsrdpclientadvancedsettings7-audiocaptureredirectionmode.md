---
title: Propiedad IMsRdpClientAdvancedSettings7 AudioCaptureRedirectionMode
description: Especifica o recupera un valor booleano que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Propiedad AudioCaptureRedirectionMode Servicios de Escritorio remoto
- Propiedad AudioCaptureRedirectionMode Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad AudioCaptureRedirectionMode
- Propiedad AudioCaptureRedirectionMode Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be6083a3b609a558830b9e7b837acce179ac7a098315b2bfeeacca800bfdc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138798"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a>Propiedad IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode

Especifica o recupera un valor booleano que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a>Valor de propiedad

Valor **VARIANT \_ BOOL** que especifica si se redirige la captura de audio. Especifique **VARIANT \_ TRUE** si desea que se redirija la captura de audio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





