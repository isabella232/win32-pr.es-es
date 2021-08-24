---
description: El método get \_ NetworkType obtiene el tipo de red.
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: Método ITConnection::get_NetworkType (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d323d7465563d0a0d400c930585c2c0df002cedfae252d205d53aea8040f337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660335"
---
# <a name="itconnectionget_networktype-method"></a>ItConnection::get \_ NetworkType (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ NetworkType** obtiene el tipo de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppNetworkType* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene el tipo de red.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppNetworkType* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                    |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                   |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppNetworkType.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection::put \_ NetworkType**](itconnection-put-networktype.md)
</dt> </dl>

 

