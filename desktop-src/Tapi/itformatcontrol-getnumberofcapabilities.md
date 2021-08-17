---
description: El método GetNumberOfCapabilities recupera el número de funcionalidades asociadas al formato actual.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: Método ITFormatControl::GetNumberOfCapabilities (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57bd79b61f8c41893ec8d99ffc9bfadcc3887631c885d5caa430a6fb723396a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945280"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>ItFormatControl::GetNumberOfCapabilities (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetNumberOfCapabilities** recupera el número de funcionalidades asociadas al formato actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwCount* \[ out\]
</dt> <dd>

Recuento de las funcionalidades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




