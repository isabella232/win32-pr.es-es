---
title: Propiedad ActiveBasicDevice IsAudioSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- Propiedad IsAudioSupported API de streaming de multimedia
- Propiedad IsAudioSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079747"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>ActiveBasicDevice:: IsAudioSupported (propiedad)

Obtiene un valor que indica si el dispositivo admite audio.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un **valor booleano** que indica si el dispositivo admite audio.

**true** si el dispositivo admite audio; en caso contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

