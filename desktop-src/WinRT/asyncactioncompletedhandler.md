---
description: Representa el método al que se llama cuando se completa una acción asincrónica.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interfaz AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 5d7e091ab250dc8b7475dbf17a1d1502cd1c4aa110106584c8c8b190c927f4aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561180"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interfaz AsyncActionCompletedHandler

Representa el método al que se llama cuando se completa una acción asincrónica.

## <a name="members"></a>Miembros

La **interfaz AsyncActionCompletedHandler** hereda de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **AsyncActionCompletedHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz AsyncActionCompletedHandler** tiene estos métodos.



| Método                                               | Descripción                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Invocar**](asyncactioncompletedhandler-invoke.md) | Invoca el método al que se llama cuando se completa la acción asincrónica especificada.<br/> |



 

## <a name="remarks"></a>Observaciones

Asigne **AsyncActionCompletedHandler** a [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) para recibir una notificación cuando se complete la acción asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

