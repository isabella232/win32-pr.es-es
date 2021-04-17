---
description: Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient:: AdviseProvider (método) (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716227"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>ITipAutocompleteClient:: AdviseProvider (método)

Registra el proveedor con el cliente para permitir que el cliente llame al objeto de proveedor de autocompletar de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
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

Puntero de interfaz a la interfaz del proveedor de autocompletar.

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

[**ITipAutocompleteClient:: UnadviseProvider (método)**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Referencia del panel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




