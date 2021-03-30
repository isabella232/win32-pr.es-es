---
title: Función RtmRegisterClient (RTM. h)
description: La función RtmRegisterClient registra un cliente como un controlador del protocolo especificado. Establece un mecanismo de notificación de cambio de ruta para el cliente y establece las opciones de protocolo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient función RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803482"
---
# <a name="rtmregisterclient-function"></a>RtmRegisterClient función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmRegisterClient** registra un cliente como un controlador del protocolo especificado. Establece un mecanismo de notificación de cambio de ruta para el cliente y establece las opciones de protocolo.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ de\]
</dt> <dd>

Especifica la familia de protocolos del Protocolo de enrutamiento que se va a registrar.

</dd> <dt>

*RoutingProtocol* \[ de\]
</dt> <dd>

Especifica el identificador del Protocolo de enrutamiento, el mismo que se usa al registrar con el administrador de enrutadores. Vea [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ de\]
</dt> <dd>

Especifica que ha cambiado la mejor ruta a una red de la tabla. El administrador de tablas de enrutamiento señala este evento después de un cambio en la mejor ruta a cualquier red de la tabla. Consulte [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) para obtener más información acerca de la notificación de cambio de ruta.

Este parámetro es opcional. Si el autor de la llamada especifica **null** para este parámetro, el administrador de tabla de enrutamiento no notifica al cliente los cambios en el mejor estado de la ruta.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Especifica varias opciones para el control especial del Protocolo de enrutamiento. Actualmente se admite el valor siguiente.



| Marcas                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**\_Protocolo RTM \_ , \_ ruta única**</dt> </dl> | El administrador de tablas de enrutamiento solo mantiene una ruta por red de destino para el protocolo de enrutamiento. En otras palabras, el administrador de tablas de enrutamiento reemplaza las entradas de ruta que tienen los mismos números de red de destino en lugar de agregar otras nuevas.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de **identificador** que identifica el cliente en llamadas posteriores al administrador de tabla de enrutamiento, si la devolución es correcta.

Un identificador **nulo** indica que el administrador de tabla de enrutamiento no pudo registrar el cliente. Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener la razón del error.



| Value                                                                                                         | Descripción                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**el \_ cliente de error \_ ya \_ existe**</dt> </dl> | Otro cliente ya se ha registrado para controlar el protocolo especificado.<br/>              |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>      | La familia de protocolos especificada no es compatible o el parámetro *Flags* no es válido.<br/> |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl>   | Recursos insuficientes para realizar la operación.<br/>                                   |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>     | Memoria insuficiente para asignar estructuras de datos para el cliente.<br/>                      |



 

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

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificadores de la familia del protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

