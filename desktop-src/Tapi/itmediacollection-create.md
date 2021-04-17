---
description: El método Create crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection:: Create (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690978"
---
# <a name="itmediacollectioncreate-method"></a>ITMediaCollection:: Create (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Create** crea un nuevo medio con propiedades predeterminadas, lo agrega a la colección en el índice especificado y devuelve un puntero a la interfaz [**ITMedia**](itmedia.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice del nuevo elemento. El valor mínimo para el índice es 1 y el valor máximo para el índice es el número actual de elementos + 1.

</dd> <dt>

*ppMedia* \[ enuncia\]
</dt> <dd>

Puntero a la interfaz [**ITMedia**](itmedia.md) creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppMedia* no es un puntero válido.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro de *Índice* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La mayoría de las listas de C y C++ están basadas en 0, pero este índice está basado en 1 para la compatibilidad de Visual Basic, lo que significa que el primer elemento tiene un número de índice de 1.

TAPI llama al método **AddRef** en la interfaz [**ITMedia**](itmedia.md) devuelta por **ITMediaCollection:: Create**. La aplicación debe llamar a **Release** en la interfaz [**ITMedia**](itmedia.md) para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




