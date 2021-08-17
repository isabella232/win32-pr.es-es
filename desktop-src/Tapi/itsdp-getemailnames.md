---
description: El método GetEmailNames obtiene una matriz de nombres de correo electrónico asociados al blob de conferencia.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: Método ITSdp::GetEmailNames (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140268"
---
# <a name="itsdpgetemailnames-method"></a>ItSdp::GetEmailNames (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método GetEmailNames** obtiene una matriz de nombres de correo electrónico asociados al blob de conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAddresses* \[ out\]
</dt> <dd>

**Puntero VARIANT** a una SAFEARRAY de **BSTR** que enumera direcciones de correo electrónico.

</dd> <dt>

*pNames* \[ out\]
</dt> <dd>

**Puntero VARIANT** a una SAFEARRAY de nombres de lista de **BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pAddresses* o *pNames* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>           |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                            |



 

## <a name="remarks"></a>Comentarios

Las listas a *las que apuntan pAddresses* y *pNames* tienen la misma longitud.

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

 

 




