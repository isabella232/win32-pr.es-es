---
description: Las constantes de marca de bits LINEPARKMODE \_ describen diferentes formas de llamadas de aparcamiento.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: LINEPARKMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3070ad3f9e56de5e4e1a026b5f779c59469e947ff55b530e9d5b414a1b3b53b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140008"
---
# <a name="lineparkmode_-constants"></a>Constantes \_ LINEPARKMODE

Las constantes de marca de bits **LINEPARKMODE \_** describen diferentes formas de llamadas de aparcamiento.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ DIRECTED**
</dt> <dd> <dl> <dt>



Especifica el aparcamiento de llamadas dirigidas. La dirección donde se va a aparpare la llamada debe proporcionarse al modificador .


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ NO DIRIGIDO**
</dt> <dd> <dl> <dt>



Especifica el aparcamiento de llamadas no dirigido. El modificador selecciona la dirección donde se apareó la llamada y la proporciona el conmutador a la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Las **constantes LINEPARKMODE \_ se usan** al aparcar una llamada. Consulte las funcionalidades del dispositivo de dirección de una línea para averiguar qué modo de aparcamiento está disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




