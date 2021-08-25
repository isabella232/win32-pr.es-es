---
description: El método get \_ Originator obtiene el originador de la conferencia.
ms.assetid: a324098d-ae22-42e9-901e-b277433af199
title: Método ITSdp::get_Originator (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4033f6008f6bb1189f53c5ac3f649ac66d74d6bd2380d9c400143cfaa8df8da9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126275"
---
# <a name="itsdpget_originator-method"></a>ItSdp::get \_ Originator (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Originator** obtiene el originador de la conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Originator(
  [out] BSTR *ppOriginator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppOriginator* \[ out\]
</dt> <dd>

Puntero a una **representación BSTR** del originador de la conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppOriginator* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppOriginator.*

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
</dt> <dt>

[**ITSdp::put \_ Originator**](itsdp-put-originator.md)
</dt> </dl>

 

