---
description: Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'ITipAutocompleteClient:: UserSelection (método) (TipAutoComplete. h)'
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
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716225"
---
# <a name="itipautocompleteclientuserselection-method"></a>ITipAutocompleteClient:: UserSelection (método)

Notifica al panel de entrada que el usuario ha seleccionado algo en la lista de autocompletar y descartar todo el texto restante que todavía no se ha insertado.

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
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a este método desde el proveedor para notificar al cliente que se ha realizado una selección por parte del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITipAutocompleteClient**](itipautocompleteclient.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




