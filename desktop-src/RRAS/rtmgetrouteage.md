---
title: Función RtmGetRouteAge (Rtm.h)
description: La función RtmGetRouteAge devuelve la antigüedad de una ruta. La edad es el tiempo, en segundos, desde que se creó o se actualizó por última vez.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- Función RAS de RtmGetRouteAge
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
ms.openlocfilehash: 03ee536eeb4d16cbfc2bbcfb7dc09cae8b0003bbd925945fa710e15cb1c4a96e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035665"
---
# <a name="rtmgetrouteage-function"></a>Función RtmGetRouteAge

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmGetRouteAge** devuelve la antigüedad de una ruta. La edad es el tiempo, en segundos, desde que se creó o se actualizó por última vez.

## <a name="syntax"></a>Sintaxis


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta* \[ En\]
</dt> <dd>

Puntero a una estructura específica de la familia de protocolos que especifica los datos de ruta obtenidos recientemente del administrador de tablas de enrutamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes valores.



| Value                                                                                   | Descripción                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**RouteAge**</dt> </dl> | Tiempo en segundos desde que se creó o actualizó por última vez una ruta.<br/>                                                                                    |
| <dl> <dt>**Infinito**</dt> </dl> | El contenido de la estructura de rutas no es válido. En este caso, una llamada a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ INVALID \_ PARAMETER.<br/> |



 

## <a name="remarks"></a>Comentarios

La antigüedad de la ruta se calcula a partir del miembro RR TimeStamp de la estructura a la que apunta \_ el *parámetro Route.* El administrador de tabla de enrutamiento establece el valor de este miembro cuando se agrega o actualiza una ruta.

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

[Referencia de la versión 1 de Routing Table Manager \_](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

