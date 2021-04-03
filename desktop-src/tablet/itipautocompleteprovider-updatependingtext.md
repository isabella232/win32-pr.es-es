---
description: Lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha tachado en el panel de entrada.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider:: UpdatePendingText (método) (TipAutoComplete. h)'
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
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083450"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>ITipAutocompleteProvider:: UpdatePendingText (método)

Lo usa el cliente de Autocompletar para notificar a la aplicación el texto que un usuario ha tachado en el panel de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPendingText* \[ de\]
</dt> <dd>

Texto de origen que se va a usar para generar la lista de autocompletar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este texto no contendrá el texto ya insertado en el campo con el foco. El proveedor de autocompletar es responsable de tener en cuenta el texto del campo actual y la selección para generar la lista de autocompletar. Cuando *bstrPendingText* es **null**, la lista de autocompletar se genera con el texto actual a la izquierda de la selección en el campo.

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

 

 




