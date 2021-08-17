---
description: El método get IsValid valida el blob del Protocolo de descriptor de sesión (SDP; consulte RFC 2327) para conocer los valores \_ de estructura y campo.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: Método ITSdp::get_IsValid (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1674b51c605354a021948a63a0e993578a3d0114e625acec2cb9e24238423c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140298"
---
# <a name="itsdpget_isvalid-method"></a>ItSdp::get \_ IsValid (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ IsValid** valida el blob del Protocolo de descriptor de sesión (SDP; consulte RFC 2327) para conocer los valores de estructura y campo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pfIsValid* \[ out\]
</dt> <dd>

Indica si la estructura del blob es válida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pfIsValid* no es válido.<br/>              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pfIsValid* no es un puntero válido.<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




