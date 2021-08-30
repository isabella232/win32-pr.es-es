---
title: Función de devolución de llamada PxeProviderRecvRequest
description: Se llama cuando se recibe una solicitud de un cliente.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Función de devolución de llamada PxeProviderRecvRequest Windows Deployment Services
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dc2ef36c26e667e55870d38f450891e9e91134c297d09ba12157452e4d01442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098655"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>Función de devolución de llamada PxeProviderRecvRequest

Se llama cuando se recibe una solicitud de un cliente. Esta función se registra mediante una llamada a [**la función PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con el parámetro *CallbackType* establecido en **PXE \_ CALLBACK \_ RECV \_ REQUEST**.

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

*hClientRequest* \[ En\]
</dt> <dd>

Controlar una solicitud recibida de un cliente.

</dd> <dt>

*pPacket* \[ En\]
</dt> <dd>

Puntero al búfer de memoria que contiene el paquete recibido.

</dd> <dt>

*uPacketLen* \[ En\]
</dt> <dd>

Longitud, en bytes, del búfer al que apunta el *parámetro pPacket.*

</dd> <dt>

*pLocalAddress* \[ En\]
</dt> <dd>

Puntero a una [**estructura DIRECCIÓN \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección local en la que se recibió el paquete.

</dd> <dt>

*pRemoteAddress* \[ En\]
</dt> <dd>

Puntero a una [**estructura DIRECCIÓN \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contiene la dirección de origen del paquete.

</dd> <dt>

*pAction* \[ out\]
</dt> <dd>

Especifica la acción que debe realizar el sistema.



| Value                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt> </dl>                | El proveedor respondió a un cliente con un paquete de respuesta DHCP estándar que contiene una ruta de acceso al programa de arranque de red. Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la [**función PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_ BA \_ CUSTOM**</dt> <dt>2</dt> </dl>       | El proveedor respondió a un cliente mediante una respuesta personalizada que no se ajusta a las especificaciones de DHCP. Devolver esta acción significa que el proveedor completó correctamente la solicitud de cliente mediante una llamada a la [**función PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) al menos una vez.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_ BA \_ IGNORE**</dt> <dt>3</dt> </dl>       | El proveedor no quiere dar servicio a la solicitud de cliente y la solicitud no debe pasarse al proveedor siguiente. Se liberan todos los recursos asociados a la solicitud de cliente y se omite la solicitud de cliente. Los proveedores también pueden usar este valor si reconocen el cliente pero la solicitud tiene un formato mal.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_ BA \_ REJECTED**</dt> <dt>4</dt> </dl> | El proveedor no quiere dar servicio a la solicitud de cliente. El sistema pasa la solicitud al siguiente proveedor de la lista de proveedores registrados. Si se trata del último proveedor de la lista, se liberan todos los recursos asociados a la solicitud de cliente y se omite la solicitud de cliente.<br/>                     |



 

</dd> <dt>

*pContext* \[ En\]
</dt> <dd>

Valor de contexto pasado a la [**función PxeRegisterCallback.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el proveedor procesó correctamente la solicitud de cliente, la devolución de llamada debe devolver **ERROR \_ SUCCESS** y la ACCIÓN DE **\_ ARRANQUE \_ PXE** a la que apunta el *parámetro pAction* contiene la acción de arranque adecuada para esta solicitud. Si el proveedor procesará la solicitud de cliente de forma asincrónica, la devolución de llamada debe devolver **ERROR \_ IO \_ PENDING** y llamar a la [**función PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) cuando se haya procesado la solicitud de cliente. En caso de error, se debe devolver un código de error adecuado y el sistema continuará como si se hubiera especificado la acción de arranque **PXE \_ BA \_ REJECTED.**

## <a name="remarks"></a>Comentarios

El tipo de paquetes que ve un proveedor se puede cambiar con la [**función PxeProviderSetAttribute.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)

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
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





