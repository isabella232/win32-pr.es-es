---
title: Propiedad VideoPlaybackMode de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica el modo de reproducción de vídeo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad VideoPlaybackMode
- Propiedad VideoPlaybackMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad VideoPlaybackMode
- Propiedad VideoPlaybackMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422627"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>IMsRdpClientAdvancedSettings7:: VideoPlaybackMode (propiedad)

Especifica o recupera un valor que indica el modo de reproducción de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Valor de propiedad

Valor que especifica el modo de reproducción de vídeo.

Los valores posibles son:

<dt>

1
</dt> <dd>

El modo de reproducción de vídeo predeterminado. Cuando el modo de reproducción de vídeo se establece en este valor, la redirección de vídeo se controla mediante la propiedad [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) . Cuando la propiedad **AudioRedirectionMode** se establece en el **modo de audio \_ \_ Redirect**, el vídeo se descodifica y se representa en el cliente.

</dd> <dt>

0
</dt> <dd>

La redirección de reproducción de vídeo está deshabilitada, incluso cuando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) está establecido en **\_ \_ redirigir el modo de audio**. En este modo, el vídeo se descodifica y se representa en el servidor host de sesión de escritorio remoto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                             |
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

 

 





