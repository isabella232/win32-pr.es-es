---
description: Establece el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction::p ut_Completed (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: aff219d5e6847c64034eed1b057e300ea601eedaa8aa7a131f1467aeacc42422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323168"
---
# <a name="iasyncactionput_completed-method"></a>Método IAsyncAction::p ut \_ Completed

Establece el método al que se llama cuando se completa la acción asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ out\]
</dt> <dd>

Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\***

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

 

 
