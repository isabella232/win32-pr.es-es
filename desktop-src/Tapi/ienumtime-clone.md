---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime:: Clone (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681000"
---
# <a name="ienumtimeclone-method"></a>IEnumTime:: Clone (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ enuncia\]
</dt> <dd>

Puntero al nuevo objeto [**IEnumTime**](ienumtime.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppEnum* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | Error por razones desconocidas.<br/>                          |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**IEnumTime**](ienumtime.md) devuelta por **IEnumTime:: Clone**. La aplicación debe llamar a **Release** en la interfaz **IEnumTime** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




