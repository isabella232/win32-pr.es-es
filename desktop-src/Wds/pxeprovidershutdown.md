---
title: Función de devolución de llamada PxeProviderShutdown
description: Se llama para cerrar el proveedor.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Función de devolución de llamada PxeProviderShutdown servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705139"
---
# <a name="pxeprovidershutdown-callback-function"></a>Función de devolución de llamada PxeProviderShutdown

Se llama para cerrar el proveedor. Esta función se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en apagado de la **\_ devolución de llamada \_ PXE**. Después de llamar a esta función, el identificador *hProvider* pasado a la función [*PxeProviderInitialize*](pxeproviderinitialize.md) ya no es válido.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ de\]
</dt> <dd>

Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el cierre del proveedor se realiza correctamente, la devolución de llamada debe devolver el **error \_ correcto**. En caso de error, se debe devolver un código de error adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de servidor de servicios de implementación de Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





