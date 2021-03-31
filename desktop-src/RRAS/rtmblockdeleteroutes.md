---
title: Función RtmBlockDeleteRoutes (RTM. h)
description: La función RtmBlockDeleteRoutes elimina todas las rutas del subconjunto especificado de rutas de la tabla.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes función RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491404"
---
# <a name="rtmblockdeleteroutes-function"></a>RtmBlockDeleteRoutes función)

\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]

La función **RtmBlockDeleteRoutes** elimina todas las rutas del subconjunto especificado de rutas de la tabla.

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

*ClientHandle* \[ de\]
</dt> <dd>

Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento, de las rutas que se van a eliminar.

</dd> <dt>

*EnumerationFlags* \[ de\]
</dt> <dd>

Especifica las rutas que se deben enumerar. Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las siguientes marcas y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* . Las marcas son las mismas que las que se usan en [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , salvo que la versión RTM \_ solo \_ \_ es redundante para **RtmBlockDeleteRoutes**. La designación de la mejor ruta se ajusta a medida que se eliminan las rutas, por lo que la función elimina finalmente todas las rutas del subconjunto.

</dd> <dt>

*CriteriaRoute* \[ de\]
</dt> <dd>

Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)). Los valores de miembro de esta estructura corresponden a las marcas especificadas por el parámetro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ sin \_ rutas**</dt> </dl>            | No hay ninguna ruta que tenga los criterios especificados.<br/>                                           |
| <dl> <dt>**ERROR \_ de \_ identificador no válido**</dt> </dl>       | El parámetro *ClientHandle* no es válido.<br/>                                                      |
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>    | Uno o varios de los parámetros de entrada no son válidos; por ejemplo, las marcas de enumeración no son válidas.<br/> |
| <dl> <dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt> </dl> | No hay suficientes recursos para realizar la operación.<br/>                                    |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl>   | No hay memoria suficiente para realizar la operación.<br/>                                        |



 

## <a name="remarks"></a>Observaciones

La función genera los mensajes de notificación adecuados a todos los clientes registrados, incluido el autor de la llamada.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





