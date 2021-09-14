---
title: Función RtmCreateEnumerationHandle (Rtm.h)
description: La función RtmCreateEnumerationHandle devuelve un identificador que se usará con RtmEnumerateGetNextRoute para examinar todas las rutas, o un subconjunto de rutas, conocidas por el administrador de tablas de enrutamiento.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Función RAS RtmCreateEnumerationHandle
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273551"
---
# <a name="rtmcreateenumerationhandle-function"></a>Función RtmCreateEnumerationHandle

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La función **RtmCreateEnumerationHandle** devuelve un identificador que se usará con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) para examinar todas las rutas, o un subconjunto de rutas, conocidas por el administrador de tablas de enrutamiento.

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

*ProtocolFamily* \[ En\]
</dt> <dd>

Especifica la familia de protocolos de las rutas que se enumeran.

</dd> <dt>

*EnumerationFlags* \[ En\]
</dt> <dd>

Especifica qué rutas se deben enumerar. Este parámetro limita el conjunto de rutas devueltas por la API de enumeración a un subconjunto definido por las marcas siguientes y los valores de los miembros correspondientes de la estructura a las que apunta el *parámetro CriteriaRoute.* Este parámetro puede ser uno de los valores siguientes.



| EnumerationFlags                                                                                                                                                                              | Significado                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <dt>**RTM \_ SOLO \_ ESTA \_ RED**</dt> </dl>       | Enumerar solo las rutas que tienen el mismo número de red que el miembro RR Network de la estructura a la que \_ apunta CriteriaRoute.<br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <dt>**RTM \_ SOLO \_ ESTA \_ INTERFAZ**</dt> </dl> | Enumerar solo las rutas obtenidas a través de la interfaz especificada por el campo RR InterfaceID de la estructura a la que \_ apunta CriteriaRoute.<br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <dt>**RTM \_ SOLO \_ ESTE \_ PROTOCOLO**</dt> </dl>    | Enumerar solo las rutas agregadas por el protocolo de enrutamiento especificado por el campo RR RoutingProtocol de la estructura a la que \_ apunta CriteriaRoute.<br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <dt>**SOLO LAS \_ MEJORES \_ \_ RUTAS DE RTM**</dt> </dl>          | Enumerar solo las mejores rutas a cada una de las redes del conjunto.<br/>                                                                                           |



 

</dd> <dt>

*CriteriaRoute* \[ En\]
</dt> <dd>

Puntero a una estructura de ruta específica de la familia de protocolos [**(RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE).**](rtm-ipx-route.md) Los valores de miembro de esta estructura corresponden a las marcas especificadas por el *parámetro EnumerationFlags.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **un IDENTIFICADOR** que se usará con las llamadas de enumeración posteriores.

Si se produce un error en la función o no existe ninguna ruta con los criterios especificados, el valor devuelto es **NULL.** Llame [**a GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.



| Value                                                                                                       | Descripción                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ SIN \_ RUTAS**</dt> </dl>            | No hay ninguna ruta que tenga los criterios especificados.<br/>                                                             |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | Uno o varios de los parámetros de entrada no son válidos (por ejemplo, familia de protocolos desconocida, marcas de enumeración no válidas).<br/> |
| <dl> <dt>**ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/>                                                      |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>   | No hay memoria suficiente para asignar el identificador.<br/>                                                              |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

