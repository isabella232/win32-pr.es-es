---
title: Función RtmGetNetworkCount (Rtm.h)
description: La función RtmGetNetworkCount recupera el número de redes a las que el administrador de tablas de enrutamiento tiene rutas.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Función RAS de RtmGetNetworkCount
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271884"
---
# <a name="rtmgetnetworkcount-function"></a>Función RtmGetNetworkCount

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmGetNetworkCount** recupera el número de redes a las que el administrador de tablas de enrutamiento tiene rutas.

## <a name="syntax"></a>Sintaxis


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ En\]
</dt> <dd>

Especifica para qué tipo de red se va a obtener información de ruta, por ejemplo, IP o IPX.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es el recuento de red, el número de redes conocidas por los protocolos de enrutamiento de la familia de protocolos especificada.

Si el valor devuelto es cero, no hay rutas disponibles o no se pudo hacer la operación. Llame [**a GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.



| Value                                                                                                    | Descripción                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NO \_ HAY NINGÚN ERROR**</dt> </dl>                 | La operación se ha hecho correctamente, pero no hay rutas disponibles.<br/>                                             |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl> | El valor del parámetro *ProtocolFamily* no corresponde a ninguna familia de protocolos instalada.<br/> |



 

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

[Identificadores de familia de protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

