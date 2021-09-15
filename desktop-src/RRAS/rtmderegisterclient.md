---
title: Función RtmDeregisterClient (Rtm.h)
description: La función RtmDeregisterClient anula el registro del cliente y libera los recursos asociados al cliente.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Función RTMDeregisterClient RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271919"
---
# <a name="rtmderegisterclient-function"></a>Función RtmDeregisterClient

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmDeregisterClient** anula el registro del cliente y libera los recursos asociados al cliente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientHandle* \[ En\]
</dt> <dd>

Identificador que identifica el cliente que se anula el registro. Para obtener este identificador, llame [**a RtmRegisterClient.**](rtmregisterclient.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**</dt> </dl>       | El *parámetro ClientHandle* no es un identificador válido.<br/> |
| <dl> <dt>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | Recursos insuficientes para llevar a cabo la operación.<br/>  |



 

## <a name="remarks"></a>Observaciones

Esta función quita todas las rutas agregadas por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





