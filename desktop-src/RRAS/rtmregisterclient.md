---
title: Función RtmRegisterClient (Rtm.h)
description: La función RtmRegisterClient registra un cliente como controlador del protocolo especificado. Establece un mecanismo de notificación de cambio de ruta para el cliente y establece opciones de protocolo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Ras de función RtmRegisterClient
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
ms.openlocfilehash: db58fc9457195c2149fd8d34a8a65a6d5085135275e1c878633f64cb742b02cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081045"
---
# <a name="rtmregisterclient-function"></a>Función RtmRegisterClient

\[Esta API ha sido reemplazada por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmRegisterClient** registra un cliente como controlador del protocolo especificado. Establece un mecanismo de notificación de cambio de ruta para el cliente y establece opciones de protocolo.

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

*ProtocolFamily* \[ En\]
</dt> <dd>

Especifica la familia de protocolos del protocolo de enrutamiento que se registrará.

</dd> <dt>

*RoutingProtocol* \[ En\]
</dt> <dd>

Especifica el identificador del protocolo de enrutamiento, el mismo que se usa al registrarse con el administrador de enrutadores. Vea [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).

</dd> <dt>

*ChangeEvent* \[ En\]
</dt> <dd>

Especifica que ha cambiado la mejor ruta a una red de la tabla. El administrador de tabla de enrutamiento señala este evento después de un cambio en la mejor ruta a cualquier red de la tabla. Consulte [**RtmDequeueRouteChangeMessage para**](rtmdequeueroutechangemessage.md) obtener más información sobre la notificación de cambio de ruta.

Este parámetro es opcional. Si el autor de la llamada especifica **NULL para** este parámetro, el administrador de tablas de enrutamiento no notifica al cliente los cambios en el mejor estado de ruta.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Especifica varias opciones para el control especial del protocolo de enrutamiento. Actualmente se admite el siguiente valor.



| Marcas                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <dt>**RUTA ÚNICA DEL PROTOCOLO RTM \_ \_ \_**</dt> </dl> | El administrador de tablas de enrutamiento mantiene solo una ruta por red de destino para el protocolo de enrutamiento. En otras palabras, el administrador de tablas de enrutamiento reemplaza las entradas de ruta que tienen los mismos números de red de destino en lugar de agregar otras nuevas.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la devolución es correcta, **un valor HANDLE** que identifica el cliente en llamadas posteriores al administrador de tablas de enrutamiento.

Un **identificador NULL** indica que el administrador de tablas de enrutamiento no pudo registrar el cliente. Llame [**a GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el motivo del error.



| Value                                                                                                         | Descripción                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**EL CLIENTE \_ DE ERROR \_ YA \_ EXISTE**</dt> </dl> | Otro cliente ya se ha registrado para controlar el protocolo especificado.<br/>              |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>      | No se admite la familia de protocolos especificada o el *parámetro Flags* no es válido.<br/> |
| <dl> <dt>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**</dt> </dl>   | Recursos insuficientes para llevar a cabo la operación.<br/>                                   |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>     | Memoria insuficiente para asignar estructuras de datos para el cliente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 del Administrador de tablas de enrutamiento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[Identificadores de familia de protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> <dt>

[**RtmDeregisterClient**](rtmderegisterclient.md)
</dt> </dl>

 

