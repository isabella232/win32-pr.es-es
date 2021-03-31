---
title: Función RtmGetRouteAge (RTM. h)
description: La función RtmGetRouteAge devuelve la antigüedad de una ruta. La antigüedad es el tiempo, en segundos, desde que se creó o actualizó por última vez.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge función RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802786"
---
# <a name="rtmgetrouteage-function"></a>RtmGetRouteAge función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmGetRouteAge** devuelve la antigüedad de una ruta. La antigüedad es el tiempo, en segundos, desde que se creó o actualizó por última vez.

## <a name="syntax"></a>Sintaxis


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta* \[ de de\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que especifica los datos de ruta obtenidos recientemente del administrador de tablas de enrutamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los valores siguientes.



| Value                                                                                   | Descripción                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ruta**</dt> </dl> | El tiempo en segundos transcurrido desde que se creó o actualizó por última vez una ruta.<br/>                                                                                    |
| <dl> <dt>**DEFINIDO**</dt> </dl> | El contenido de la estructura de ruta no es válido. En este caso, una llamada a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un \_ parámetro de error no válido \_ .<br/> |



 

## <a name="remarks"></a>Observaciones

La antigüedad de la ruta se calcula a partir del \_ miembro de marca de tiempo RR de la estructura a la que apunta el parámetro *Route* . El administrador de tablas de enrutamiento establece el valor de este miembro cuando se agrega o se actualiza una ruta.

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

[Referencia de la versión 1 del administrador de tablas de enrutamiento \_](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de la versión 1 del administrador de tablas de enrutamiento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> <dt>

[**\_ruta IPX de RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

