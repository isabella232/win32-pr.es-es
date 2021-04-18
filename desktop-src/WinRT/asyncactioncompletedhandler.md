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
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715157"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interfaz AsyncActionCompletedHandler

Representa el método al que se llama cuando se completa una acción asincrónica.

## <a name="members"></a>Miembros

La interfaz **AsyncActionCompletedHandler** hereda de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **AsyncActionCompletedHandler** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **AsyncActionCompletedHandler** tiene estos métodos.



| Método                                               | Descripción                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Invocar**](asyncactioncompletedhandler-invoke.md) | Invoca el método al que se llama cuando se completa la acción asincrónica especificada.<br/> |



 

## <a name="remarks"></a>Observaciones

Asigne un **AsyncActionCompletedHandler** a un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) para recibir una notificación cuando se complete la acción asincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                    |
| Encabezado<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

