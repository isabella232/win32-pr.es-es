---
description: El método get \_ EnumerationIf obtiene un puntero a una interfaz de enumeración de medios.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: Método ITMediaCollection::get_EnumerationIf (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe14475e216b5143b599aab50d12d1d0c548b5f64dd8e44edd2e6aab249905c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060863"
---
# <a name="itmediacollectionget_enumerationif-method"></a>ItMediaCollection::get \_ EnumerationIf (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ EnumerationIf** obtiene un puntero a una interfaz de enumeración de medios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a la [**interfaz IEnumMedia**](ienummedia.md) del elemento deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVal* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Este método es intercambiable con [**get \_ \_ NewEnum,**](itmediacollection-get--newenum.md) salvo que devuelve [**IEnumMedia**](ienummedia.md) en lugar de **IUnknown.**

TAPI llama al **método AddRef** en la [**interfaz IEnumMedia**](ienummedia.md) devuelta por **ITMediaCollection::get \_ Enumerationlf**. La aplicación debe llamar **a Release** en la **interfaz IEnumMedia** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




