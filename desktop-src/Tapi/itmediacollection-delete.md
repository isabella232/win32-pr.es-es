---
description: El método Delete elimina el medio correspondiente al índice especificado.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ITMediaCollection::D método iminar (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680506"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection::D iminar (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Delete** elimina el medio correspondiente al índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice de los medios que se van a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                                              | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                                     | El método se realizó correctamente.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | El parámetro de *Índice* tiene un valor menor que 1 o mayor que el número actual de elementos.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                            | No hay memoria suficiente para realizar la operación.<br/>                                          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                                   | Error interno (solo se debe producir si una llamada anterior ha devuelto un error).<br/>                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                                | Este método aún no se ha implementado.<br/>                                                           |
| <dl> <dt>**HRESULT \_ del \_ código de error \_ (SDPBLB \_ conf \_ BLOB \_ destruido)**</dt> </dl> | El BLOB SDP no existe.<br/>                                                                   |



 

## <a name="remarks"></a>Observaciones

La mayoría de las listas de C y C++ están basadas en 0, pero este índice está basado en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




