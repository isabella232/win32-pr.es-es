---
title: Función de devolución de llamada PxeProviderRecvRequest
description: Se le llama cuando se recibe una solicitud de un cliente.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Función de devolución de llamada PxeProviderRecvRequest servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422316"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>Función de devolución de llamada PxeProviderRecvRequest

Se le llama cuando se recibe una solicitud de un cliente. Esta función se registra mediante una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en **\_ \_ \_ solicitud de devolución de llamada de PXE**.

## <a name="syntax"></a>Sintaxis


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hClientRequest* \[ de\]
</dt> <dd>

Identificador de una solicitud recibida de un cliente.

</dd> <dt>

*pPacket* \[ de\]
</dt> <dd>

Puntero al búfer de memoria que contiene el paquete recibido.

</dd> <dt>

*uPacketLen* \[ de\]
</dt> <dd>

Longitud, en bytes, del búfer al que apunta el parámetro *pPacket* .

</dd> <dt>

*pLocalAddress* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ direcciones de PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección local en la que se recibió el paquete.

</dd> <dt>

*pRemoteAddress* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ direcciones de PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección de origen del paquete.

</dd> <dt>

*pAction* \[ enuncia\]
</dt> <dd>

Especifica la acción que debe realizar el sistema.



| Value                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt> </dl>                | El proveedor respondió a un cliente con un paquete de respuesta DHCP estándar que contiene una ruta de acceso al programa de arranque de red. Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la función [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_ BA \_ personalizado**</dt> <dt>2</dt> </dl>       | El proveedor respondió a un cliente mediante una respuesta personalizada que no se ajusta a las especificaciones de DHCP. Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la función [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_ BA \_ omitir**</dt> <dt>3</dt> </dl>       | El proveedor no desea atender la solicitud del cliente y la solicitud no debe pasarse al siguiente proveedor. Se liberan todos los recursos asociados a la solicitud del cliente y se omite la solicitud del cliente. Los proveedores también pueden usar este valor si reconocen el cliente pero la solicitud tiene un formato incorrecto.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_ BA \_ rechazado**</dt> <dt>4</dt> </dl> | El proveedor no desea atender la solicitud del cliente. El sistema pasa la solicitud al siguiente proveedor de la lista de proveedores registrados. Si este era el último proveedor de la lista, se liberarán todos los recursos asociados a la solicitud del cliente y se omitirá la solicitud del cliente.<br/>                     |



 

</dd> <dt>

*pContext* \[ de\]
</dt> <dd>

Valor de contexto que se pasa a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el proveedor ha procesado correctamente la solicitud de cliente, la devolución de llamada debe devolver el **error \_ Success** y la **\_ \_ acción de arranque de PXE** a la que apunta el parámetro *pAction* contiene la acción de arranque adecuada para esta solicitud. Si el proveedor va a procesar la solicitud de cliente de forma asincrónica, la devolución de llamada debe devolver la **\_ e/s de error \_ pendiente** y llamar a la función [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) cuando se haya procesado la solicitud de cliente. En caso de error, se debe devolver un código de error adecuado y el sistema continuará como si se hubiera especificado la acción de arranque de la operación **PXE \_ BA \_ rechazada** .

## <a name="remarks"></a>Observaciones

El tipo de paquetes que detecta un proveedor se puede cambiar con la función [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .

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
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





