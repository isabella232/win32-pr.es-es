---
title: Función de devolución de llamada PxeProviderShutdown
description: Se llama para apagar el proveedor.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Función de devolución de llamada PxeProviderShutdown Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5efc7267a5b5e1c15d185b96419210f31981c56c887dd5a8ab7f1068eb4f20ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860795"
---
# <a name="pxeprovidershutdown-callback-function"></a>Función de devolución de llamada PxeProviderShutdown

Se llama para apagar el proveedor. Esta función se registra mediante una llamada a [**la función PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en **PXE \_ CALLBACK \_ SHUTDOWN**. Después de llamar a esta función, el *identificador hProvider* pasado a la [*función PxeProviderInitialize*](pxeproviderinitialize.md) ya no es válido.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ En\]
</dt> <dd>

Valor de contexto pasado a la [**función PxeRegisterCallback.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el cierre del proveedor se realiza correctamente, la devolución de llamada debe devolver **ERROR \_ SUCCESS**. En caso de error, se debe devolver un código de error adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 solo con aplicaciones de escritorio sp2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Funciones del servidor de Servicios de implementación](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





