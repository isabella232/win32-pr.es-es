---
description: Las \_ constantes de marcador de bits LINEPARKMODE describen diferentes formas de llamadas de estacionamiento.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes de LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690752"
---
# <a name="lineparkmode_-constants"></a>Constantes de LINEPARKMODE \_

Las constantes de marcador de bits **LINEPARKMODE \_** describen diferentes formas de llamadas de estacionamiento.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ dirigido**
</dt> <dd> <dl> <dt>



Especifica el estacionamiento de llamadas dirigido. La dirección en la que se va a detener la llamada se debe proporcionar al conmutador.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE no \_ Directed**
</dt> <dd> <dl> <dt>



Especifica el parque de llamadas no directas. El modificador selecciona la dirección en la que se ha detenido la llamada y la proporciona el modificador a la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Las **\_ constantes LINEPARKMODE** se usan cuando se estaciona una llamada. Consulte las capacidades del dispositivo de dirección de una línea para averiguar qué modo de estacionamiento está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




