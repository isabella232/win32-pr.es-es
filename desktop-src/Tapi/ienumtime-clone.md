---
description: 'Método IEnumTime::Clone: el método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: Método IEnumTime::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8deb34e6fea6ec08cb15b42b3952c34a73edad27fbcae268d1b99addb54f5438
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865759"
---
# <a name="ienumtimeclone-method"></a>IEnumTime::Clone (Método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntero al nuevo [**objeto IEnumTime.**](ienumtime.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppEnum* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Error por motivos desconocidos.<br/>                          |



 

## <a name="remarks"></a>Comentarios

TAPI llama al **método AddRef** en la [**interfaz IEnumTime devuelta**](ienumtime.md) por **IEnumTime::Clone**. La aplicación debe llamar **a Release** en la **interfaz IEnumTime** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




