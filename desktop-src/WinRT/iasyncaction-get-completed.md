---
description: Obtiene el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: IAsyncAction::get_Completed método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 90e26947f0771490334ee731b25576759943c44cc47a9fda6681da9aa1f11fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323447"
---
# <a name="iasyncactionget_completed-method"></a>IAsyncAction::get \_ Completed (método)

Obtiene el método al que se llama cuando se completa la acción asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ out\]
</dt> <dd>

Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

Método que controla la notificación de finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
