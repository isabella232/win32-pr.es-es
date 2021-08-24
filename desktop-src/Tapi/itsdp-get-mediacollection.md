---
description: El método get \_ MediaCollection obtiene un puntero a la interfaz ITMediaCollection para la conferencia.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: Método ITSdp::get_MediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774515"
---
# <a name="itsdpget_mediacollection-method"></a>ITSdp::get \_ MediaCollection (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ MediaCollection** obtiene un puntero a la [**interfaz ITMediaCollection**](itmediacollection.md) para la conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMediaCollection* \[ out\]
</dt> <dd>

Puntero a [**ITMediaCollection.**](itmediacollection.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                            | El método se realizó correctamente.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | El *parámetro ppMediaCollection* no es un puntero válido.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | No existe memoria suficiente para realizar la operación.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Error no especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ ERROR \_ CODE(ERROR \_ INVALID \_ DATA)**</dt> </dl> | Se ha producido un error interno, normalmente debido al error de un método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método aún no se ha implementado.<br/>                                              |



 

## <a name="remarks"></a>Comentarios

También se puede obtener un puntero [**ITMediaCollection**](itmediacollection.md) mediante **QueryInterface**.

TAPI llama al **método AddRef** en la [**interfaz ITMediaCollection**](itmediacollection.md) devuelta por **ITSdp::get \_ MediaCollection**. La aplicación debe llamar a **Release en** la **interfaz ITMediaCollection** para liberar recursos asociados a ella.

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




