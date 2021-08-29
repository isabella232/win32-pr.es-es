---
description: Muestra u oculta la lista de autocompletar.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: Método ITipAutocompleteProvider::Show (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2afc5fc264df4d38e85dfa3374714b06908eee8ec1c5517b49dc32cbcbd44f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716464"
---
# <a name="itipautocompleteprovidershow-method"></a>ITipAutocompleteProvider::Show (método)

Muestra u oculta la lista de autocompletar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fShow* \[ En\]
</dt> <dd>

**TRUE** para mostrar la interfaz de usuario autocompletar, **FALSE** para ocultar la interfaz de usuario de la lista de autocompletar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

El cliente llama a este método para mostrar u ocultar la lista de autocompletar. Si no se muestra la lista autocompletar y *fShow* es **FALSE,** este método no hace nada. Si se muestra la lista autocompletar y *fShow* es **TRUE,** este método no hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITipAutocompleteProvider (interfaz)**](itipautocompleteprovider.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




