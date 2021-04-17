---
description: Las \_ constantes de marcador de bits LINEADDRESSSHARING describen varias maneras en que se puede compartir una dirección entre las líneas.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes de LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680250"
---
# <a name="lineaddresssharing_-constants"></a>Constantes de LINEADDRESSSHARING \_

Las constantes de marcador de bits **LINEADDRESSSHARING \_** describen varias maneras en que se puede compartir una dirección entre las líneas.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privado**
</dt> <dd> <dl> <dt>



La dirección es privada para la línea del usuario; no se asigna a ninguna otra estación.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



La dirección se enlaza a una o varias estaciones. La primera línea para activar una llamada en la línea tendrá acceso exclusivo a la dirección y llamadas que pueden existir en ella. Otras líneas no podrán usar la dirección de puente mientras esté en uso.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



La dirección se enlaza con una o varias estaciones. La primera línea para activar una llamada en la línea tendrá acceso exclusivo únicamente a la llamada correspondiente. Otras aplicaciones que utilizan la dirección darán lugar a una apariencia de llamada nueva y separada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



La dirección se enlaza con una o varias líneas. Todas las entidades puente pueden compartirse en llamadas en la dirección, que, a continuación, funciona como una conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ supervisado**
</dt> <dd> <dl> <dt>



Se trata de una dirección cuyo estado de inactividad se pone a disposición de esta línea.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

La forma en que una dirección se comparte entre las líneas puede afectar al comportamiento de esa dirección. [**Línea \_ de**](line-callstate.md) Los mensajes CALLSTATE y [**\_ ADDRESSSTATE de línea**](line-addressstate.md) se envían a la aplicación en respuesta a las actividades de las estaciones de puente. A través de estos mensajes, una aplicación puede realizar un seguimiento del estado de la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LÍNEA \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




