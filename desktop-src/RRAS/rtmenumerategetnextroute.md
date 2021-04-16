---
title: Función RtmEnumerateGetNextRoute (RTM. h)
description: La función RtmEnumerateGetNextRoute devuelve la entrada de ruta siguiente en la enumeración iniciada por una llamada a RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute función RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676833"
---
# <a name="rtmenumerategetnextroute-function"></a>RtmEnumerateGetNextRoute función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmEnumerateGetNextRoute** devuelve la entrada de ruta siguiente en la enumeración iniciada por una llamada a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnumerationHandle* \[ de\]
</dt> <dd>

Identificador que identifica la enumeración y especifica su ámbito. Obtenga este identificador llamando a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Ruta* \[ de enuncia\]
</dt> <dd>

Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)). Esta estructura recibirá la siguiente ruta en la enumeración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ identificador no válido**</dt> </dl>       | El parámetro *EnumerationHandle* no es válido.<br/>              |
| <dl> <dt>**ERROR: \_ no hay \_ más \_ rutas**</dt> </dl>      | No hay más rutas en la enumeración.<br/>                 |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Aunque las rutas no se devuelven en ningún orden concreto, cada ruta en la enumeración se devuelve una sola vez.

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

[**\_ruta IP de RTM \_**](rtm-ip-route.md)
</dt> <dt>

[**\_ruta IPX de RTM \_**](rtm-ipx-route.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





