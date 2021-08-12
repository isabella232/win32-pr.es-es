---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient.h)
description: Los clientes de cumplimiento usan para procesar un SoHResponse cada vez que reciben un blob de datos SoHResponse del servidor de cumplimiento.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Método NAP de ProcessSoHResponse
- Método NAP de ProcessSoHResponse, interfaz INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP , ProcessSoHResponse method
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cffd2caeaf3a39bd5c28b4850fc560dc9567a3552aad88929581efd2729acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621714"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>Método INapEnforcementClientBinding::P rocessSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los clientes de cumplimiento usan el método **INapEnforcementClientBinding::P rocessSoHResponse** para procesar soHResponse cada vez que reciben un blob de datos SoHResponse del servidor de cumplimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexión* \[ En\]
</dt> <dd>

Puntero COM a la [**interfaz INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión de cliente. NapAgent no contiene referencias al objeto asociado a esta interfaz una vez completada esta llamada al método.

Debe usar una conexión establecida previamente para procesar blobs de datos SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok (Aceptar)**</dt> </dl>                   | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | No se han creado conexiones previamente en el cliente de cumplimiento. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | El límite de recursos del sistema no pudo realizar la operación.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**PAQUETE NAP \_ E \_ NO \_ VÁLIDO**</dt> </dl>  | Si se devuelve este valor, el cliente de cumplimiento debe quitar el paquete si NapAgent devuelve NAP \_ E \_ INVALID \_ PACKET. En este caso, el ejecutor debe asumir que el servidor con el que está hablando no está habilitado para NAP y quitar la conexión de la lista activa (es decir, notificar a NapAgent un estado de conexión fuera de servicio).<br/> |
| <dl> <dt>**NAP \_ E NO COINCIDE \_ \_ ID**</dt> </dl>   | Si se devuelve este valor, indica que el identificador de correlación del paquete SoH-Response no coincide con el soH-response pendiente. En este caso, el ejecutor debe quitar el paquete y esperar otro paquete SoH-Response más reciente.<br/> Esto puede deberse a una respuesta a un mensaje de solicitud anterior.<br/>        |
| <dl> <dt>**NAP \_ E \_ NO \_ INICIALIZADO**</dt> </dl> | El ejecutor no se ha inicializado previamente.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

NapAgent consulta el blob SoH-Response datos del objeto de conexión, lo procesa y establece la decisión resultante (por ejemplo, acceso completo o restringido/etc.) en el objeto de conexión.

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la [**interfaz INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





