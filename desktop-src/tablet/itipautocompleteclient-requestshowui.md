---
description: Determina si el Panel de entrada está listo para que se muestra la lista autocompletar.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: Método ITipAutocompleteClient::RequestShowUI (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579444"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>ITipAutocompleteClient::RequestShowUI (método)

Determina si el Panel de entrada está listo para que se muestra la lista autocompletar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWndACList* \[ En\]
</dt> <dd>

Identificador de ventana de la interfaz de usuario de lista de autocompletar.

</dd> <dt>

*pfAllowShowing* \[ out\]
</dt> <dd>

**FALSE** si el cliente recomienda no mostrar la interfaz de usuario de la lista de autocompletar. **TRUE** si el proveedor de autocompletar puede mostrar la interfaz de usuario de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El proveedor de autocompletar llama a este método cuando está a punto de mostrar la interfaz de usuario autocompletar. Si el estado interno del cliente no permite que el proveedor muestre la interfaz de usuario, *pfAllowShowing* se establecerá en **FALSE.** Por ejemplo, cuando el texto se envía al campo desde la máscara de escritura a mano en el panel de entrada de Tablet PC y el usuario empieza a infieren inmediatamente, el cliente recomendará no mostrar la interfaz de usuario autocompletar, para evitar la destructuración de la entrada manuscrita del usuario, estableciendo *pfAllowShowing* en **FALSE.**

Llame **a RequestShowUI** para establecer el identificador de ventana de lista de autocompletar emergente antes de llamar al método [**ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md). Si no lo hace, se producirá un error **E \_ INVALIDARG** al llamar a **PreferredRects**.

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

[**ITipAutocompleteClient::P referredRects (Método)**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




