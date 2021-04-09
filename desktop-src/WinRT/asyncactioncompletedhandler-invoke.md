---
description: Invoca el método al que se llama cuando se completa la acción asincrónica especificada.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'AsyncActionCompletedHandler:: Invoke (método)'
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
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154311"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a>AsyncActionCompletedHandler:: Invoke (método)

Invoca el método al que se llama cuando se completa la acción asincrónica especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*asyncInfo* \[ de\]
</dt> <dd>

Tipo: **[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _

La acción asincrónica que informa de la finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)
</dt> </dl>

 

