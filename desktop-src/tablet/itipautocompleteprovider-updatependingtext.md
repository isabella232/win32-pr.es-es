---
description: Lo usa el cliente de autocompletar para notificar a la aplicación el texto que un usuario ha escrito en el Panel de entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: Método ITipAutocompleteProvider::UpdatePendingText (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 99fc67b5ba6495e2bdfb8a54de2412ca01cbdd37475d08d20d227b203f2da1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716435"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>ITipAutocompleteProvider::UpdatePendingText (método)

Lo usa el cliente de autocompletar para notificar a la aplicación el texto que un usuario ha escrito en el Panel de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPendingText* \[ En\]
</dt> <dd>

Texto de origen que se usará para generar la lista de autocompletar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este texto no contendrá el texto ya insertado en el campo centrado. El proveedor de autocompletar es responsable de tener en cuenta el texto del campo actual y la selección para generar la lista de autocompletar. Cuando *bstrPendingText es* **NULL,** se genera la lista autocompletar con el texto actual a la izquierda de la selección en el campo .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITipAutocompleteProvider (interfaz)**](itipautocompleteprovider.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




