---
description: El método \_ get Item obtiene un puntero ITMedia correspondiente al índice especificado.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: Método ITMediaCollection::get_Item (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160648"
---
# <a name="itmediacollectionget_item-method"></a>ITMediaCollection::get \_ Item (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ get Item** obtiene un puntero [**ITMedia**](itmedia.md) correspondiente al índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del elemento multimedia que se obtiene.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a la [**interfaz ITMedia**](itmedia.md) del elemento deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVal* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Index* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

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

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




