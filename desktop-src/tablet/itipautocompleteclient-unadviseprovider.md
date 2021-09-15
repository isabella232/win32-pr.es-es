---
description: Anula el registro del proveedor asociado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: Método ITipAutocompleteClient::UnadviseProvider (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579441"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>ITipAutocompleteClient::UnadviseProvider (método)

Anula el registro del proveedor asociado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWndField* \[ En\]
</dt> <dd>

Identificador de ventana del campo que proporciona la característica autocompletar.

</dd> <dt>

*pIACProvider* \[ En\]
</dt> <dd>

Puntero de interfaz a la interfaz del proveedor autocompletar que se va a anular el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

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

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




