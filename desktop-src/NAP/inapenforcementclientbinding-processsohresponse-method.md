---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Lo usan los clientes de cumplimiento para procesar un SoHResponse cada vez que reciben un BLOB de datos SoHResponse del servidor de cumplimiento.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método ProcessSoHResponse
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
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535530"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding::P método rocessSoHResponse

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los clientes de cumplimiento usan el método **INapEnforcementClientBinding::P rocesssohresponse** para procesar un SoHResponse cada vez que reciben un BLOB de datos SoHResponse del servidor de cumplimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexión* \[ de de\]
</dt> <dd>

Puntero COM a la interfaz [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la conexión de cliente. El NapAgent no conserva las referencias al objeto asociado a esta interfaz después de que se complete esta llamada al método.

Debe usar una conexión establecida previamente para procesar los blobs de datos SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

También se pueden devolver otros códigos de error específicos de COM.



| Código devuelto                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>                   | La operación se realizó correctamente.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | No se han creado previamente conexiones en el cliente de cumplimiento. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Error de permisos, acceso denegado.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Límite de recursos del sistema, no se pudo realizar la operación.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_paquete NAP E \_ no válido \_**</dt> </dl>  | Si se devuelve este valor, el cliente de cumplimiento debe quitar el paquete si NapAgent devuelve \_ un \_ paquete no válido de NAP \_ . En este caso, el exiginte debe asumir que el servidor al que se está comunicando no está habilitado para NAP y quitar la conexión de la lista activa (es decir, notificar a NapAgent de un estado de conexión inactivo).<br/> |
| <dl> <dt>**identificador de NAP \_ E no \_ coincidente \_**</dt> </dl>   | Si se devuelve este valor, indica que el identificador de correlación del paquete SoH-Response no coincidía con la respuesta de SoH pendiente. En este caso, el exiginte debe quitar el paquete y esperar a otro paquete de SoH-Response más reciente.<br/> Esto puede deberse a una respuesta a un mensaje de solicitud anterior.<br/>        |
| <dl> <dt>**NAP \_ E \_ no \_ inicializado**</dt> </dl> | El exigidor no se ha inicializado previamente.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

NapAgent consulta el BLOB de datos SoH-Response del objeto de conexión, lo procesa y establece la decisión resultante (por ejemplo, acceso completo/restringido/etc.) en el objeto de conexión.

El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





