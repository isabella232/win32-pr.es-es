---
description: Anula el registro del proveedor asociado.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'ITipAutocompleteClient:: UnadviseProvider (método) (TipAutoComplete. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910438"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>ITipAutocompleteClient:: UnadviseProvider (método)

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

*hWndField* \[ de\]
</dt> <dd>

Identificador de ventana del campo que proporciona la característica Autocompletar.

</dd> <dt>

*pIACProvider* \[ de\]
</dt> <dd>

Puntero de interfaz a la interfaz del proveedor de autocompletar cuya registro se va a anular.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

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

 

 




