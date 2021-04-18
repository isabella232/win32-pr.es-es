---
title: Función de devolución de llamada PxeProviderServiceControl
description: Se llama cuando el servicio WDS recibe un código de control de servicio.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Función de devolución de llamada PxeProviderServiceControl servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705140"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>Función de devolución de llamada PxeProviderServiceControl

Se llama cuando el servicio WDS recibe un código de control de servicio. Esta función de devolución de llamada se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en el **control de servicio de devolución de \_ llamada \_ \_ PXE**.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ de\]
</dt> <dd>

Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> <dt>

*dwControl* 
</dt> <dd>

Código de control. Para obtener la lista de valores posibles, vea el parámetro *dwControl* de la función [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .

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

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

