---
title: Propiedad ActiveBasicDevice IsSearchSupported (PlayToDevice. h)
description: Obtiene un valor que indica si el dispositivo admite la búsqueda.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- Propiedad IsSearchSupported API de streaming de multimedia
- Propiedad IsSearchSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422587"
---
# <a name="activebasicdeviceissearchsupported-property"></a>ActiveBasicDevice:: IsSearchSupported (propiedad)

Obtiene un valor que indica si el dispositivo admite la búsqueda.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un **valor booleano** que indica si el dispositivo admite la búsqueda.

**true** si el dispositivo admite la búsqueda; en caso contrario, **false**.

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

 

