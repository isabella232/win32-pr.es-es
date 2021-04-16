---
description: El \_ método get MediaCollection obtiene un puntero a la interfaz ITMediaCollection para la Conferencia.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Método ITSdp:: get_MediaCollection (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679315"
---
# <a name="itsdpget_mediacollection-method"></a>ITSdp:: get \_ MediaCollection (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ MediaCollection** obtiene un puntero a la interfaz [**ITMediaCollection**](itmediacollection.md) para la Conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMediaCollection* \[ enuncia\]
</dt> <dd>

Puntero a [**ITMediaCollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                                                           | Significado                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                            | El método se realizó correctamente.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | El parámetro *ppMediaCollection* no es un puntero válido.<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | No hay memoria suficiente para realizar la operación.<br/>                             |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                                          | Error no especificado.<br/>                                                               |
| <dl> <dt>**HRESULT \_ del \_ código de ERROR \_ (error de \_ datos no válidos \_ )**</dt> </dl> | Se ha producido un error interno, normalmente debido a un error en un método anterior.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                                       | Este método aún no se ha implementado.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

También se puede obtener un puntero [**ITMediaCollection**](itmediacollection.md) mediante **QueryInterface**.

TAPI llama al método **AddRef** en la interfaz [**ITMediaCollection**](itmediacollection.md) devuelta por **ITSdp:: get \_ MediaCollection**. La aplicación debe llamar a **Release** en la interfaz **ITMediaCollection** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




