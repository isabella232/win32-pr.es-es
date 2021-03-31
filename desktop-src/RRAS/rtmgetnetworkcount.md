---
title: Función RtmGetNetworkCount (RTM. h)
description: La función RtmGetNetworkCount recupera el número de redes a las que el administrador de tabla de enrutamiento tiene rutas.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount función RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802209"
---
# <a name="rtmgetnetworkcount-function"></a>RtmGetNetworkCount función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmGetNetworkCount** recupera el número de redes a las que el administrador de tabla de enrutamiento tiene rutas.

## <a name="syntax"></a>Sintaxis


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ de\]
</dt> <dd>

Especifica para qué tipo de red se va a obtener información de ruta, por ejemplo, IP o IPX.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es el recuento de redes, el número de redes conocidas para los protocolos de enrutamiento de la familia de protocolos especificada.

Si el valor devuelto es cero, no hay ninguna ruta disponible o se produjo un error en la operación. Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.



| Value                                                                                                    | Descripción                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SIN \_ errores**</dt> </dl>                 | La operación se realizó correctamente, pero no hay ninguna ruta disponible.<br/>                                             |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl> | El valor del parámetro *ProtocolFamily* no se corresponde con ninguna familia de protocolos instalada.<br/> |



 

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

[Identificadores de la familia del protocolo RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

