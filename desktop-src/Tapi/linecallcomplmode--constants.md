---
description: Las constantes de marca de bits LINECALLCOMPLMODE describen diferentes maneras en las que \_ se puede completar una llamada.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761759"
---
# <a name="linecallcomplmode_-constants"></a>LineCALLCOMPLMODE \_ (Constantes)

Las constantes de marca de bits **LINECALLCOMPLMODE \_** describen diferentes maneras en las que se puede completar una llamada.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**DEVOLUCIÓN DE LLAMADA LINECALLCOMPLMODE \_**
</dt> <dd> <dl> <dt>



Solicita a la estación llamada que devuelva la llamada cuando vuelva a estar inactiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**
</dt> <dd> <dl> <dt>



Pone en cola la llamada hasta que se puede completar la llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**
</dt> <dd> <dl> <dt>



Agrega la aplicación a la llamada existente en la estación llamada (ir a la estación).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE \_ MESSAGE**
</dt> <dd> <dl> <dt>



Deja un mensaje predefinido corto para la estación llamada (Dejar llamada a Word). El mensaje que se va a enviar se especifica por separado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




