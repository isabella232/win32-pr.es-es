---
title: Propiedad AudioQualityMode de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido. De forma predeterminada, se establece en 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioQualityMode
- Propiedad AudioQualityMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AudioQualityMode
- Propiedad AudioQualityMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686032"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7:: AudioQualityMode (propiedad)

Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido. De forma predeterminada, se establece en 0.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Valor de propiedad

Valor que especifica el modo de calidad de audio.

Los valores posibles son:

<dt>

0
</dt> <dd>

Calidad de audio dinámica. Esta es la configuración de calidad de audio predeterminada. El servidor ajusta dinámicamente la calidad de salida de audio en respuesta a las condiciones de red y a las capacidades de cliente y servidor.

</dd> <dt>

1
</dt> <dd>

Calidad de audio media. El servidor usa un formato fijo pero comprimido para la salida de audio.

</dd> <dt>

2
</dt> <dd>

Calidad de audio alta. El servidor proporciona una salida de audio en formato PCM sin comprimir con una sobrecarga de procesamiento menor para la latencia.

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

 

 





