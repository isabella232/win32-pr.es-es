---
title: Propiedad IMsRdpClientAdvancedSettings7 AudioQualityMode
description: Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido. De forma predeterminada, se establece en 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Propiedad AudioQualityMode Servicios de Escritorio remoto
- Propiedad AudioQualityMode Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad AudioQualityMode
- Propiedad AudioQualityMode Servicios de Escritorio remoto interfaz , IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad AudioQualityMode
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
ms.openlocfilehash: 1635c2ed01144a640b624a014959a4847ae5f746502267444d958a20b959eef9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001313"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7::AudioQualityMode, propiedad

Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido. De forma predeterminada, se establece en 0.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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

Calidad de audio dinámico. Esta es la configuración de calidad de audio predeterminada. El servidor ajusta dinámicamente la calidad de salida de audio en respuesta a las condiciones de red y las funcionalidades de cliente y servidor.

</dd> <dt>

1
</dt> <dd>

Calidad de audio media. El servidor usa un formato fijo pero comprimido para la salida de audio.

</dd> <dt>

2
</dt> <dd>

Alta calidad de audio. El servidor proporciona salidas de audio en formato PCM sin comprimir con una menor sobrecarga de procesamiento para la latencia.

</dd> </dl>

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

 

 





