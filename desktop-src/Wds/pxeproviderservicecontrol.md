---
title: Función de devolución de llamada PxeProviderServiceControl
description: Se llama cuando el servicio WDS recibe un código de control de servicio.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Función de devolución de llamada PxeProviderServiceControl Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 406152025518a7fb3bb50e0b44fea72bbd17b5cafbc6907912499b70eae1d5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999595"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>Función de devolución de llamada PxeProviderServiceControl

Se llama cuando el servicio WDS recibe un código de control de servicio. Esta función de devolución de llamada se registra mediante una llamada a la [**función PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en **PXE \_ CALLBACK \_ SERVICE \_ CONTROL**.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ En\]
</dt> <dd>

Valor de contexto pasado a la [**función PxeRegisterCallback.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)

</dd> <dt>

*dwControl* 
</dt> <dd>

Código de control. Para obtener la lista de valores posibles, vea el *parámetro dwControl* de la [*función HandlerEx.*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)

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

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

