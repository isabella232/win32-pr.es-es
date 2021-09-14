---
title: Método IMsTscAxEvents OnRemoteWindowDisplayed
description: Se llama cuando se muestra una ventana remoteapp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnRemoteWindowDisplayed
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259084"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a>Método IMsTscAxEvents::OnRemoteWindowDisplayed

Se llama cuando se muestra una ventana remoteapp.

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

*vbDisplayed* \[ En\]
</dt> <dd>

Tipo: **VARIANT \_ BOOL**

Indica si se muestra u oculta la ventana RemoteApp.

</dd> <dt>

*hwnd* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana que se muestra.

</dd> <dt>

*windowAttribute* \[ En\]
</dt> <dd>

Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**

Valor de la [**enumeración RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica más información sobre el evento.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)
</dt> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





