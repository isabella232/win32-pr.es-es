---
description: Obtiene el método al que se llama cuando se completa la acción asincrónica.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'IAsyncAction:: get_Completed (método)'
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
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154307"
---
# <a name="iasyncactionget_completed-method"></a>IAsyncAction:: get \_ completed (método)

Obtiene el método al que se llama cuando se completa la acción asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*controlador* \[ de enuncia\]
</dt> <dd>

Tipo: **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***

El método que controla la notificación de finalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

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

 

 
