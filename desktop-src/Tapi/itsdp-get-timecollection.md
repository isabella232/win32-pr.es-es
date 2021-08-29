---
description: El método get \_ TimeCollection obtiene un puntero a una interfaz ITTimeCollection para la conferencia.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: Método ITSdp::get_TimeCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d52760de1cac36206269d9e3d890bb9383ce331a11d061c74a8c047ee01010b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060843"
---
# <a name="itsdpget_timecollection-method"></a>ItSdp::get \_ TimeCollection (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ TimeCollection** obtiene un puntero a una [**interfaz ITTimeCollection**](ittimecollection.md) para la conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTimeCollection* \[ out\]
</dt> <dd>

Puntero a [**ITTimeCollection**](ittimecollection.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | El método se realizó correctamente.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | El *parámetro ppTimeCollection* no es un puntero válido.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | No existe memoria suficiente para realizar la operación.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Error no especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ ERROR \_ CODE(ERROR \_ INVALID \_ DATA)**</dt> </dl> | Se ha producido un error interno, normalmente debido al error de un método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método aún no se ha implementado.<br/>                                              |



 

## <a name="remarks"></a>Comentarios

También se puede obtener un puntero [**ITTimeCollection**](ittimecollection.md) mediante **QueryInterface**.

TAPI llama al **método AddRef** en la [**interfaz ITTimeCollection**](ittimecollection.md) devuelta por **ITSdp::get \_ TimeCollection**. La aplicación debe llamar a **Release** en la **interfaz ITTimeCollection** para liberar recursos asociados a ella.

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

[**ITTimeCollection**](ittimecollection.md)
</dt> </dl>

 

 




