---
description: El método get Ttl obtiene el ámbito de período de \_ vida (TTL) para las transmisiones en las direcciones.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: ItConnection::get_Ttl (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0522098f9959f3595d3deae83161fece53ad95353b9e41a60e653980353b22ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003383"
---
# <a name="itconnectionget_ttl-method"></a>ItConnection::get \_ Ttl (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Ttl** obtiene el [*ámbito de*](t-tapgloss.md) período de vida (TTL) para las transmisiones en las direcciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTtl* \[ out\]
</dt> <dd>

Ámbito de TTL.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pTtl* no es un puntero válido.<br/>         |
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

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




