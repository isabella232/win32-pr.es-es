---
description: El método Create crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: ItMediaCollection::Create (método, Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a2b11624b6a22a9bf1bff7b87538d3c7e915892a4ec7b816ee3d6c4d03821d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060873"
---
# <a name="itmediacollectioncreate-method"></a>ITMediaCollection::Create (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Create** crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz [**ITMedia.**](itmedia.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del nuevo elemento. El valor mínimo del índice es 1 y el valor máximo del índice es el número actual de elementos + 1.

</dd> <dt>

*ppMedia* \[ out\]
</dt> <dd>

Puntero a [**la interfaz ITMedia**](itmedia.md) creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppMedia* no es un puntero válido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Index* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La mayoría de las listas de C y C++ se basan en 0, pero este índice se basa en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.

TAPI llama al **método AddRef** en la [**interfaz ITMedia**](itmedia.md) devuelta por **ITMediaCollection::Create**. La aplicación debe llamar a **Release en** la [**interfaz ITMedia**](itmedia.md) para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




