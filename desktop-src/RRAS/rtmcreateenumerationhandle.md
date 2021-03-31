---
title: Función RtmCreateEnumerationHandle (RTM. h)
description: La función RtmCreateEnumerationHandle devuelve un identificador que se utiliza con RtmEnumerateGetNextRoute para examinar todas las rutas, o un subconjunto de rutas, conocido por el administrador de tabla de enrutamiento.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle función RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150011"
---
# <a name="rtmcreateenumerationhandle-function"></a>RtmCreateEnumerationHandle función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmCreateEnumerationHandle** devuelve un identificador que se utiliza con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) para examinar todas las rutas, o un subconjunto de rutas, conocido por el administrador de tabla de enrutamiento.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ de\]
</dt> <dd>

Especifica la familia de protocolos de las rutas que se van a enumerar.

</dd> <dt>

*EnumerationFlags* \[ de\]
</dt> <dd>

Especifica las rutas que se deben enumerar. Este parámetro limita el conjunto de rutas devueltas por la API de enumeración a un subconjunto definido por los siguientes marcadores y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* . Este parámetro puede ser uno de los valores siguientes.



| EnumerationFlags                                                                                                                                                                              | Significado                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**RTM \_ solo \_ esta \_ red**</dt> </dl>       | Enumerar solo las rutas que tienen el mismo número de red que el \_ miembro de red RR de la estructura a la que apunta CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**RTM \_ solo \_ esta \_ interfaz**</dt> </dl> | Enumerar solo las rutas obtenidas a través de la interfaz especificada por el \_ campo RR InterfaceID de la estructura a la que apunta CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**RTM \_ solo \_ este \_ Protocolo**</dt> </dl>    | Enumerar solo las rutas agregadas por el protocolo de enrutamiento especificado por el \_ campo RR RoutingProtocol de la estructura a la que apunta CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**\_solo las \_ mejores \_ rutas de RTM**</dt> </dl>          | Enumerar solo las mejores rutas a cada una de las redes del conjunto.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ de\]
</dt> <dd>

Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)). Los valores de miembro de esta estructura corresponden a las marcas especificadas por el parámetro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un **identificador** que se va a usar con llamadas de enumeración posteriores.

Si se produce un error en la función o no existe ninguna ruta con los criterios especificados, el valor devuelto es **null**. Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.



| Value                                                                                                       | Descripción                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ sin \_ rutas**</dt> </dl>            | No hay ninguna ruta que tenga los criterios especificados.<br/>                                                             |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | Uno o varios de los parámetros de entrada no son válidos (por ejemplo, una familia de protocolos desconocida, marcas de enumeración no válidas).<br/> |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/>                                                      |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>   | No hay memoria suficiente para asignar el identificador.<br/>                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> <dt>

[**\_ruta IPX de RTM \_**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

