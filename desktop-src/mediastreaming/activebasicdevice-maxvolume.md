---
title: Propiedad ActiveBasicDevice MaxVolume (PlayToDevice. h)
description: Obtiene el volumen máximo compatible con el dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- Propiedad MaxVolume API de streaming de multimedia
- Propiedad MaxVolume API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492982"
---
# <a name="activebasicdevicemaxvolume-property"></a>ActiveBasicDevice:: MaxVolume (propiedad)

Obtiene el volumen máximo compatible con el dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un **UINT32** que especifica el volumen máximo admitido por el dispositivo.

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

 

