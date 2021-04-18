---
title: Función RtmGetNextRoute (RTM. h)
description: La función RtmGetNextRoute devuelve la siguiente ruta del subconjunto especificado de rutas de la tabla.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute función RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534474"
---
# <a name="rtmgetnextroute-function"></a>RtmGetNextRoute función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmGetNextRoute** devuelve la siguiente ruta del subconjunto especificado de rutas de la tabla.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProtocolFamily* \[ de\]
</dt> <dd>

Especifica la familia de rutas del protocolo que se va a recuperar, por ejemplo, IP o IPX.

</dd> <dt>

*EnumerationFlags* \[ de\]
</dt> <dd>

Especifica las rutas que se deben enumerar. Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las siguientes marcas y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* . Las marcas son las mismas que las que se usan en [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Ruta* \[ de in, out\]
</dt> <dd>

En la entrada, la *ruta* apunta a una estructura específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).

La función de llamada proporciona valores de miembro para esta estructura. Estos valores, junto con el parámetro *EnumerationFlags* , especifican el conjunto del que se van a devolver las rutas.

En la salida, la *ruta* apunta a una estructura que recibe la primera ruta que coincidía con los criterios especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto **no es un \_ error**.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | Uno de los parámetros no es válido.<br/>                            |
| <dl> <dt>**ERROR \_ sin \_ rutas**</dt> </dl>            | No hay ninguna ruta que coincida con los criterios especificados.<br/>       |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Las rutas se devuelven en el orden siguiente:

1.  Número de red
2.  Protocolo de enrutamiento
3.  Identificador de interfaz
4.  Dirección de próximo salto

Esta función es menos eficaz que las funciones de identificador de enumeración correspondientes.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





