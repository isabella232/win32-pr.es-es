---
title: Propiedad ActiveBasicDevice IsImageSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite imágenes.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- Propiedad IsImageSupported API de streaming de multimedia
- Propiedad IsImageSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695868"
---
# <a name="activebasicdeviceisimagesupported-property"></a>ActiveBasicDevice:: IsImageSupported (propiedad)

Obtiene un valor que indica si el dispositivo admite imágenes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un **valor booleano** que indica si el dispositivo admite imágenes.

**true** si el dispositivo admite imágenes; en caso contrario, **false**.

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

 

