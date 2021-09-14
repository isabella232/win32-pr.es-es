---
description: El método Delete elimina los medios correspondientes al índice especificado.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ItMediaCollection::D elete (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160660"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection::D elete (método)

\[Los controles e interfaces de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Delete** elimina los medios correspondientes al índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice de medios que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                                                              | Descripción                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                     | El método se realizó correctamente.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | El *parámetro Index* tiene un valor menor que 1 o mayor que el número actual de elementos.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                            | No existe memoria suficiente para realizar la operación.<br/>                                          |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                                   | Error interno (solo debe producirse si una llamada anterior devolvió un error).<br/>                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                                | Este método aún no se ha implementado.<br/>                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ ERROR \_ CODE(SDPBLB \_ CONF \_ BLOB \_ DESTROYED)**</dt> </dl> | El blob SDP no existe.<br/>                                                                   |



 

## <a name="remarks"></a>Observaciones

La mayoría de las listas de C y C++ se basan en 0, pero este índice se basa en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




