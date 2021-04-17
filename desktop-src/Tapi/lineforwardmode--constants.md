---
description: Las \_ constantes de marcador de bits LINEFORWARDMODE describen las condiciones en las que se pueden reenviar las llamadas a una dirección.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Constantes de LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691048"
---
# <a name="lineforwardmode_-constants"></a>Constantes de LINEFORWARDMODE \_

Las constantes de marcador de bits **LINEFORWARDMODE \_** describen las condiciones en las que se pueden reenviar las llamadas a una dirección.

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ ocupado**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas en ocupado, independientemente de su origen. Use este valor al reenviar para llamadas internas y externas en ocupado y no se puede controlar por separado ninguna respuesta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas externas en ocupado. Use este valor al reenviar para llamadas internas y externas en ocupado y si no hay ninguna respuesta, se puede controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas internas en ocupado. Use este valor al reenviar para llamadas internas y externas en ocupado y si no hay ninguna respuesta, se puede controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas en ocupado/sin respuesta, independientemente de su origen. Use este valor al reenviar para llamadas internas y externas en ocupado y no se puede controlar por separado ninguna respuesta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas externas en ocupado/sin respuesta. Use este valor cuando el reenvío de llamadas esté ocupado y no se pueda controlar por separado para las llamadas internas.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas internas en ocupado/no responde. Use este valor cuando el reenvío de llamadas esté ocupado y no se pueda controlar por separado para las llamadas internas.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**
</dt> <dd> <dl> <dt>



Avanzar en ocupado/no responder todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**
</dt> <dd> <dl> <dt>



Adelanta el uso de todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas sin respuesta, independientemente de su origen. Use este valor cuando no se pueda controlar por separado las llamadas internas y externas en ninguna respuesta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas externas sin respuesta. Use este valor cuando el reenvío de llamadas internas y externas sin respuesta se pueda controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas internas sin respuesta. Use este valor cuando el reenvío de llamadas internas y externas sin respuesta se pueda controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**
</dt> <dd> <dl> <dt>



Reenviar en no responder todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE no \_ disponible**
</dt> <dd> <dl> <dt>



Se reenvían las llamadas, pero las condiciones en las que se producirá el reenvío no se conocen y el proveedor de servicios nunca las conocerá. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE no \_ Cond**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas de manera incondicional, independientemente de su origen. Use este valor cuando el reenvío incondicional para llamadas internas y externas no se puede controlar por separado. El reenvío incondicional invalida el reenvío de condiciones de respuesta y/o ausencia de respuesta.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas externas de forma incondicional. Use este valor cuando el reenvío incondicional para llamadas internas y externas se puede controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**
</dt> <dd> <dl> <dt>



Reenviar todas las llamadas internas incondicionalmente. Use este valor cuando el reenvío incondicional para llamadas internas y externas se puede controlar por separado.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**
</dt> <dd> <dl> <dt>



Reenviar incondicionalmente todas las llamadas que se originaron en una dirección especificada (reenvío selectivo de llamadas).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ desconocido**
</dt> <dd> <dl> <dt>



Las llamadas se reenvían, pero en este momento no se conocen las condiciones en las que se producirá el reenvío. Es posible que las condiciones se conozcan en el futuro. (Versiones de TAPI 1,4 y posteriores)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Las marcas de bits definidas por LINEFORWARDMODE \_ no son ortogonales. El reenvío incondicional omite cualquier condición específica, como busy o no responde. Si el reenvío incondicional no está en vigor, el reenvío en ocupado y sin respuesta se puede controlar por separado o no por separado. Si se controla por separado, las \_ marcas LINEFORWARDMODE busy y LINEFORWARDMODE \_ NOANSW se pueden usar por separado. Si no se controla por separado, \_ se debe usar la marca LINEFORWARDMODE BUSYNA. Del mismo modo, si el reenvío de llamadas internas y externas se puede controlar por separado, se \_ \_ pueden usar las marcas externas LINEFORWARDMODE internas y LINEFORWARDMODE por separado; de lo contrario, se usa la combinación.

Las capacidades de dirección indican qué modos de reenvío están disponibles para cada dirección asignada a una línea. Una aplicación puede utilizar [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) para establecer condiciones de reenvío en el conmutador.

Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar estos valores de LINEFORWARDMODE \_ si la versión negociada no los admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




