---
description: Las \_ constantes de marcador de bits LINEANSWERMODE describen cómo se ve afectada una llamada activa existente en un dispositivo de línea respondiendo a otra llamada de oferta en la misma línea.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes de LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681092"
---
# <a name="lineanswermode_-constants"></a>Constantes de LINEANSWERMODE \_

Las constantes de marcador de bits **LINEANSWERMODE \_** describen cómo se ve afectada una llamada activa existente en un dispositivo de línea respondiendo a otra llamada de *oferta* en la misma línea.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**\_quitar LINEANSWERMODE**
</dt> <dd> <dl> <dt>



La llamada activa se quitará automáticamente.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_**
</dt> <dd> <dl> <dt>



La llamada activa se colocará automáticamente en espera.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ ninguno**
</dt> <dd> <dl> <dt>



Responder a otra llamada en la misma línea no tiene ningún efecto en la llamada activa existente en la línea.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Si una llamada entra en (se ofrece) en el momento en que otra llamada ya está activa, la nueva llamada se conecta a mediante la invocación de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). El efecto que tiene en la llamada activa existente depende de las capacidades del dispositivo de la línea. La primera llamada puede no verse afectada, se puede quitar automáticamente o puede colocarse automáticamente en espera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




