---
title: Función RtmGetFirstRoute (Rtm.h)
description: La función RtmGetFirstRoute devuelve la primera ruta del subconjunto de rutas especificado en la tabla.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- Función RAS de RtmGetFirstRoute
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12539e0e04422fca2f759d751c37e7a8d36828afe8017ba9a058bf0d850990d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073835"
---
# <a name="rtmgetfirstroute-function"></a>Función RtmGetFirstRoute

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

La **función RtmGetFirstRoute** devuelve la primera ruta del subconjunto de rutas especificado en la tabla.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmGetFirstRoute(
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

Especifica los límites del conjunto de rutas eliminadas a un subconjunto definido por estas marcas y los valores de los miembros correspondientes de la estructura a los que apunta el *parámetro CriteriaRoute.* Las marcas son las mismas que las usadas [**en RtmCreateEnumerationHandle.**](rtmcreateenumerationhandle.md)

</dd> <dt>

*Ruta* \[ in, out\]
</dt> <dd>

En la entrada, *la ruta* apunta a una estructura específica de la familia de protocolos [**(RTM \_ IP \_ ROUTE**](rtm-ip-route.md) o [**\_ RTM IPX \_ ROUTE).**](rtm-ipx-route.md)

La función que realiza la llamada proporciona valores de miembro para esta estructura. Estos valores, junto con el parámetro *EnumerationFlags,* especifican el conjunto desde el que se devolverán las rutas.

Salida, *Ruta apunta* a la primera ruta que coincidió con los criterios especificados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Valor                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>    | Uno de los parámetros no es válido.<br/>                            |
| <dl> <dt>**ERROR \_ SIN \_ RUTAS**</dt> </dl>            | No hay rutas que coincidan con los criterios especificados.<br/>       |
| <dl> <dt>**ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Las rutas se devuelven en el orden siguiente:

1.  Número de red
2.  Protocolo de enrutamiento
3.  Identificador de interfaz
4.  Dirección del próximo salto

Esta función es menos eficaz que la función de identificador de enumeración correspondiente, [**RtmEnumerateGetNextRoute.**](rtmenumerategetnextroute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Header<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetNextRoute**](rtmgetnextroute.md)
</dt> </dl>

 

 





