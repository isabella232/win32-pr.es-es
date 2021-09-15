---
title: Función RtmGetNextRoute (Rtm.h)
description: La función RtmGetNextRoute devuelve la siguiente ruta del subconjunto de rutas especificado en la tabla.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- Función RTMGetNextRoute RAS
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271879"
---
# <a name="rtmgetnextroute-function"></a>Función RtmGetNextRoute

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmGetNextRoute** devuelve la siguiente ruta del subconjunto de rutas especificado en la tabla.

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

*ProtocolFamily* \[ En\]
</dt> <dd>

Especifica la familia de protocolos de rutas que se recuperarán, por ejemplo, IP o IPX.

</dd> <dt>

*EnumerationFlags* \[ En\]
</dt> <dd>

Especifica qué rutas se deben enumerar. Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las marcas siguientes y los valores de los miembros correspondientes de la estructura a los que apunta *el parámetro CriteriaRoute.* Las marcas son las mismas que las usadas [**en RtmCreateEnumerationHandle.**](rtmcreateenumerationhandle.md)

</dd> <dt>

*Ruta* \[ in, out\]
</dt> <dd>

En la entrada, *Route* apunta a una estructura específica de la familia de protocolos [**(RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)).

La función de llamada proporciona valores de miembro para esta estructura. Estos valores, junto con el parámetro *EnumerationFlags,* especifican el conjunto desde el que se devuelven las rutas.

En la salida, *Route* apunta a una estructura que recibe la primera ruta que coincide con los criterios especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto **es NO \_ ERROR**.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | Uno de los parámetros no es válido.<br/>                            |
| <dl> <dt>**ERROR \_ SIN \_ RUTAS**</dt> </dl>            | No hay rutas que coincidan con los criterios especificados.<br/>       |
| <dl> <dt>**ERROR \_ NO HAY RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Las rutas se devuelven en el orden siguiente:

1.  Número de red
2.  Protocolo de enrutamiento
3.  Identificador de interfaz
4.  Dirección del próximo salto

Esta función es menos eficaz que las funciones de identificador de enumeración correspondientes.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





