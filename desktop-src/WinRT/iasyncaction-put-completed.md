---
description: Establece el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction::p ut_Completed método
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
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001151"
---
# <a name="iasyncactionput_completed-method"></a>IAsyncAction: \_ método completado:p UT

Establece el método al que se llama cuando se completa la acción asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ de enuncia\]
</dt> <dd>

Tipo: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) \** _

El método que controla la notificación de finalización.

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

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
