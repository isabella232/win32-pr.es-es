---
description: Muestra u oculta la lista de autocompletar.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider:: Show (método) (TipAutoComplete. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818110"
---
# <a name="itipautocompleteprovidershow-method"></a>ITipAutocompleteProvider:: Show (método)

Muestra u oculta la lista de autocompletar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fShow* \[ de\]
</dt> <dd>

**True** para mostrar la interfaz de usuario de autocompletar, **false** para ocultar la interfaz de usuario de la lista de autocompletar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El cliente llama a este método para mostrar u ocultar la lista de autocompletar. Si no se muestra la lista Autocompletar y *fShow* es **false**, este método no hace nada. Si se muestra la lista Autocompletar y *fShow* es **true**, este método no hace nada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete. h (también requiere Peninputpanel \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




