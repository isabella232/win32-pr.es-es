---
title: Función RtmBlockDeleteRoutes (Rtm.h)
description: La función RtmBlockDeleteRoutes elimina todas las rutas del subconjunto especificado de rutas de la tabla.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Función RAS de RtmBlockDeleteRoutes
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271935"
---
# <a name="rtmblockdeleteroutes-function"></a>Función RtmBlockDeleteRoutes

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmBlockDeleteRoutes** elimina todas las rutas del subconjunto especificado de rutas de la tabla.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ClientHandle* \[ En\]
</dt> <dd>

Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento, de las rutas que se eliminarán.

</dd> <dt>

*EnumerationFlags* \[ En\]
</dt> <dd>

Especifica qué rutas se deben enumerar. Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las marcas siguientes y los valores de los miembros correspondientes de la estructura a los que apunta *el parámetro CriteriaRoute.* Las marcas son las mismas que las usadas en [**RtmCreateEnumerationHandle,**](rtmcreateenumerationhandle.md) salvo que RTM ONLY BEST ROUTES es redundante para \_ \_ \_ **RtmBlockDeleteRoutes.** La designación de mejor ruta se ajusta a medida que se eliminan las rutas, por lo que la función finalmente elimina todas las rutas del subconjunto.

</dd> <dt>

*CriteriaRoute* \[ En\]
</dt> <dd>

Puntero a una estructura de ruta específica de la familia de protocolos [**(RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**RTM \_ IPX \_ ROUTE).**](rtm-ipx-route.md) Los valores de miembro de esta estructura corresponden a las marcas especificadas por el *parámetro EnumerationFlags.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ SIN \_ RUTAS**</dt> </dl>            | No hay ninguna ruta que tenga los criterios especificados.<br/>                                           |
| <dl> <dt>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**</dt> </dl>       | El *parámetro ClientHandle* no es válido.<br/>                                                      |
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | Uno o varios de los parámetros de entrada no son válidos, por ejemplo, las marcas de enumeración no son válidas.<br/> |
| <dl> <dt>**ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/>                                    |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl>   | No hay memoria suficiente para llevar a cabo la operación.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

La función genera los mensajes de notificación adecuados a todos los clientes registrados, incluido el autor de la llamada.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





