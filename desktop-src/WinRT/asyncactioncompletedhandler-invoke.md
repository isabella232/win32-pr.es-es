---
description: Invoca el método al que se llama cuando se completa la acción asincrónica especificada.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: Método AsyncActionCompletedHandler::Invoke
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: f106dca9d1d01b2da12ffb527f3556a0a44cf535167e5af79adbd69e4a097055
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898655"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a>Método AsyncActionCompletedHandler::Invoke

Invoca el método al que se llama cuando se completa la acción asincrónica especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*asyncInfo* \[ En\]
</dt> <dd>

Tipo: **[ **IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\***

Acción asincrónica que informa de la finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)
</dt> </dl>

 

