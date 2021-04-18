---
title: Propiedad ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice. h)
description: Obtiene un valor que indica si se admite el establecimiento del código fuente siguiente.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- Propiedad IsSetNextSourceSupported API de streaming de multimedia
- Propiedad IsSetNextSourceSupported API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, propiedad IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714632"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>ActiveBasicDevice:: IsSetNextSourceSupported (propiedad)

Obtiene un valor que indica si se admite el establecimiento del código fuente siguiente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un **valor booleano** que indica si se admite el establecimiento del código fuente siguiente.

**true** si se admite el establecimiento del código fuente siguiente; en caso contrario, **false**.

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

 

