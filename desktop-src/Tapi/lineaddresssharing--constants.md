---
description: Las constantes de marca de bits LINEADDRESSSHARING describen varias maneras de \_ compartir una dirección entre líneas.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: LINEADDRESSSHARING_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249999"
---
# <a name="lineaddresssharing_-constants"></a>LINEADDRESSSHARING \_ (Constantes)

Las constantes de marca de bits **LINEADDRESSSHARING \_** describen varias maneras de compartir una dirección entre líneas.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ PRIVATE**
</dt> <dd> <dl> <dt>



La dirección es privada para la línea del usuario; no se asigna a ninguna otra estación.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



La dirección se une a una o varias estaciones. La primera línea para activar una llamada en la línea tendrá acceso exclusivo a la dirección y a las llamadas que puedan existir en ella. Otras líneas no podrán usar la dirección de puente mientras esté en uso.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



La dirección se une con una o varias estaciones. La primera línea para activar una llamada en la línea tendrá acceso exclusivo solo a la llamada correspondiente. Otras aplicaciones que usan la dirección darán como resultado apariencias de llamadas nuevas e independientes.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



La dirección se une con una o más líneas. Todas las partes puente pueden compartir llamadas en la dirección , que luego funciona como una conferencia.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ SUPERVISADO**
</dt> <dd> <dl> <dt>



Se trata de una dirección cuyo estado inactivo o ocupado está disponible para esta línea.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

La manera en que una dirección se comparte entre líneas puede afectar al comportamiento de esa dirección. [**LINE \_ Los mensajes CALLSTATE**](line-callstate.md) [**y LINE \_ ADDRESSSTATE**](line-addressstate.md) se envían a la aplicación en respuesta a las actividades de las estaciones de puente. A través de estos mensajes, una aplicación puede realizar un seguimiento del estado de la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> </dl>

 

 




