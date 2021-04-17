---
description: El método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'IEnumMedia:: Clone (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691012"
---
# <a name="ienummediaclone-method"></a>IEnumMedia:: Clone (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ enuncia\]
</dt> <dd>

Puntero al nuevo objeto [**IEnumMedia**](ienummedia.md) .

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

TAPI llama al método **AddRef** en la interfaz [**IEnumMedia**](ienummedia.md) devuelta por **IEnumMedia:: Clone**. La aplicación debe llamar a **Release** en la interfaz **IEnumMedia** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




