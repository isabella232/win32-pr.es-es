---
description: Determina si el panel de entrada está listo para mostrar la lista de autocompletar.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient:: RequestShowUI (método) (TipAutoComplete. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277213"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>ITipAutocompleteClient:: RequestShowUI (método)

Determina si el panel de entrada está listo para mostrar la lista de autocompletar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWndACList* \[ de\]
</dt> <dd>

Identificador de ventana de la interfaz de usuario de la lista de autocompletar.

</dd> <dt>

*pfAllowShowing* \[ enuncia\]
</dt> <dd>

**False** si el cliente recomienda no mostrar la interfaz de usuario de la lista de autocompletar. **True** si el proveedor de autocompletar puede mostrar la interfaz de usuario de la lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El proveedor de autocompletar llama a este método cuando está a punto de mostrar la interfaz de usuario de autocompletar. Si el estado interno del cliente no permite al proveedor Mostrar la interfaz de usuario, *pfAllowShowing* se establecerá en **false**. Por ejemplo, cuando el texto se envía al campo desde la máscara de escritura a mano en el panel de entrada de Tablet PC y el usuario inicia inmediatamente el lápiz, el cliente recomienda no mostrar la interfaz de usuario de autocompletar, con el fin de evitar la destrucción del lápiz del usuario, estableciendo *pfAllowShowing* en **false**.

Llame a **RequestShowUI** para establecer el identificador de la ventana Lista de autocompletar emergente antes de llamar al [**método referredrects de ITipAutocompleteClient::P**](itipautocompleteclient-preferredrects.md). Si no lo hace, se producirá un error de **E \_ INVALIDARG** al llamar a **PreferredRects**.

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

[**ITipAutocompleteClient::P método referredRects**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




