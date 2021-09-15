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
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579429"
---
# <a name="itipautocompleteprovidershow-method"></a>ITipAutocompleteProvider::Show (Método)

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

**TRUE** para mostrar la interfaz de usuario autocompletar, **FALSE** para ocultar la interfaz de usuario de lista de autocompletar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El cliente llama a este método para mostrar u ocultar la lista de autocompletar. Si no se muestra la lista autocompletar y *fShow* es **FALSE,** este método no hace nada. Si se muestra la lista autocompletar y *fShow* es **TRUE,** este método no hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITipAutocompleteProvider (interfaz)**](itipautocompleteprovider.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




