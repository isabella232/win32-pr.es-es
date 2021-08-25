---
description: Notifica al Panel de entrada que el usuario ha seleccionado algo en la lista autocompletar y que descarta todo el texto restante que aún no se ha insertado.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: Método ITipAutocompleteClient::UserSelection (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2dac765c3f1c3e709bb7066a1645c2d77783ea555bccd81f9d5809da802d7043
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843485"
---
# <a name="itipautocompleteclientuserselection-method"></a>ITipAutocompleteClient::UserSelection (método)

Notifica al Panel de entrada que el usuario ha seleccionado algo en la lista autocompletar y que descarta todo el texto restante que aún no se ha insertado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

Se llama a este método desde el proveedor para notificar al cliente que el usuario ha realizado una selección.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITipAutocompleteClient (interfaz)**](itipautocompleteclient.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




