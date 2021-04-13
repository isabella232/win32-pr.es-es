---
title: IMsTscAxEvents OnRemoteWindowDisplayed, método
description: Se le llama cuando se muestra una ventana de RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422424"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>IMsTscAxEvents:: OnRemoteWindowDisplayed (método)

Se le llama cuando se muestra una ventana de RemoteApp.

## <a name="syntax"></a>Sintaxis


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vbDisplayed* \[ de\]
</dt> <dd>

Tipo: **variante \_ bool**

Indica si la ventana de RemoteApp se muestra u oculta.

</dd> <dt>

*hWnd* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana que se muestra.

</dd> <dt>

*windowAttribute* \[ de\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Un valor de la enumeración [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica más información sobre el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





