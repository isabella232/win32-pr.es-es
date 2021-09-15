---
description: Permite al cliente sugerir dónde colocar la lista de autocompletar para evitar que se superponga el Panel de entrada.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: Método ITipAutocompleteClient::P referredRects (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579445"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient::P referredRects (método)

Permite al cliente sugerir dónde colocar la lista de autocompletar para evitar que se superponga el Panel de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prcACList* \[ En\]
</dt> <dd>

Rectángulo, en coordenadas de pantalla, que indica la ubicación preferida del proveedor y el tamaño de la interfaz de usuario de lista de autocompletar.

</dd> <dt>

*prcField* \[ En\]
</dt> <dd>

Rectángulo, en coordenadas de pantalla, que indica la ubicación y el tamaño del campo centrado.

</dd> <dt>

*prcModified* \[ out\]
</dt> <dd>

Rectángulo basado en el estado actual de TIP y la ubicación y el tamaño de la lista de autocompletar preferidos especificados por *prcACList.*

</dd> <dt>

*pfShownAboveTip* \[ in, out\]
</dt> <dd>

**TRUE** si el rectángulo modificado se va a mostrar encima del área de destino del Panel de entrada de texto; de lo contrario, **FALSE**. Este valor debe inicializarse en la orientación preferida del proveedor antes de llamar al método .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Llame al [**método ITipAutocompleteClient::RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer la ventana emergente de lista de autocompletar antes de llamar al método [**ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md).<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Se ha producido un error no especificado.<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Este es el método al que llama el proveedor de autocompletar cuando está a punto de mostrar la interfaz de usuario autocompletar. El cliente modifica el rectángulo preferido del proveedor especificado por *prcACList a* través *del argumento prcModified.*

Llame al [**método ITipAutocompleteClient::RequestShowUI**](itipautocompleteclient-requestshowui.md) para establecer el identificador de ventana de lista de autocompletar emergente antes de llamar a **PreferredRects**. Si no lo hace, se producirá un error **E \_ INVALIDARG** al llamar a **PreferredRects**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                       |
| Encabezado<br/>                   | <dl> <dt>TipAutoComplete.h (también requiere Peninputpanel \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITipAutocompleteClient (interfaz)**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient::RequestShowUI (Método)**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




