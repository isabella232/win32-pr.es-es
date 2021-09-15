---
title: Función RtmIsRoute (Rtm.h)
description: La función RtmIsRoute determina si existe una o varias rutas a una red de destino especificada. Si es así, la función devuelve información para la mejor ruta a esa red.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Ras de función RtmIsRoute
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271863"
---
# <a name="rtmisroute-function"></a>Función RtmIsRoute

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmIsRoute** determina si existe una o varias rutas a una red de destino especificada. Si es así, la función devuelve información para la mejor ruta a esa red.

## <a name="syntax"></a>Sintaxis


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ En\]
</dt> <dd>

Especifica el tipo de estructura de datos al que apunta el *parámetro Network,* por ejemplo, [**IP \_ NETWORK**](ip-network.md)o [**IPX \_ NETWORK.**](ipx-network.md)

</dd> <dt>

*Red* \[ En\]
</dt> <dd>

Puntero a una estructura que especifica datos de número de red específicos de la familia de protocolos. Estos datos identifican la red para la que el autor de la llamada busca información de ruta.

</dd> <dt>

*BestRoute* \[ out\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que recibe la mejor información de ruta actual, si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los códigos siguientes.



| Value                                                                                                       | Descripción                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VERDAD**</dt> </dl>                         | Existe al menos una ruta a la red especificada. La mejor ruta se devuelve en la estructura a la que apunta el *parámetro BestRoute.*<br/>      |
| <dl> <dt>**FALSO**</dt> </dl>                        | No hay ninguna ruta a la red especificada o se ha producido un error en la operación. Llame [**a GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información:<br/> |
| <dl> <dt>**NO \_ HAY NINGÚN ERROR**</dt> </dl>                    | La operación se ha producido correctamente, pero no hay ninguna ruta a la red especificada.<br/>                                                                      |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | El valor del parámetro *ProtocolFamily* no corresponde a ninguna familia de protocolos instalada.<br/>                                             |
| <dl> <dt>**ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/>                                                                                  |



 

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

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RED \_ IP**](ip-network.md)
</dt> <dt>

[**IPX \_ NETWORK**](ipx-network.md)
</dt> <dt>

[Identificadores de familia de protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

