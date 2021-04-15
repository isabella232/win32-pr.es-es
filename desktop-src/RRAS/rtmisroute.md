---
title: Función RtmIsRoute (RTM. h)
description: La función RtmIsRoute determina si existen una o varias rutas a una red de destino especificada. Si es así, la función devuelve información para la mejor ruta a esa red.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute función RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492113"
---
# <a name="rtmisroute-function"></a>RtmIsRoute función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmIsRoute** determina si existen una o varias rutas a una red de destino especificada. Si es así, la función devuelve información para la mejor ruta a esa red.

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

*ProtocolFamily* \[ de\]
</dt> <dd>

Especifica el tipo de estructura de datos al que apunta el parámetro de *red* , por ejemplo, [**\_ red IP**](ip-network.md), [**\_ red IPX**](ipx-network.md).

</dd> <dt>

*Red* \[ de de\]
</dt> <dd>

Puntero a una estructura que especifica los datos de número de red específicos de la familia de protocolos. Estos datos identifican la red para la que el autor de la llamada busca información de ruta.

</dd> <dt>

*BestRoute* \[ enuncia\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que recibe la mejor información de ruta actual, si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes códigos.



| Value                                                                                                       | Descripción                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>                         | Existe al menos una ruta a la red especificada. La mejor ruta se devuelve en la estructura a la que apunta el parámetro *BestRoute* .<br/>      |
| <dl> <dt>**ES**</dt> </dl>                        | No hay ninguna ruta a la red especificada o se produjo un error en la operación. Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información:<br/> |
| <dl> <dt>**SIN \_ errores**</dt> </dl>                    | La operación se realizó correctamente, pero no hay ninguna ruta a la red especificada.<br/>                                                                      |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | El valor del parámetro *ProtocolFamily* no se corresponde con ninguna familia de protocolos instalada.<br/>                                             |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/>                                                                                  |



 

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

[**\_red IP**](ip-network.md)
</dt> <dt>

[**\_red IPX**](ipx-network.md)
</dt> <dt>

[Identificadores de la familia del protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

