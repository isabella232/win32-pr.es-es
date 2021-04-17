---
title: Propiedad SoundEffects
description: Propiedad SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714159"
---
# <a name="soundeffects-property"></a>Propiedad SoundEffects

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor booleano que indica si los efectos de sonido (. WAV) los archivos configurados como parte de las acciones de un carácter se reproducirán.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente * * *. AudioOutput.SoundEffects**



| Value     | Descripción                          |
|-----------|--------------------------------------|
| **True**  | Los efectos de sonido de carácter están habilitados. |
| **False** | El efecto de sonido de caracteres está deshabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad refleja la opción reproducir efectos sonoros de caracteres en la página salida de la hoja de propiedades del agente (opciones avanzadas de caracteres). Cuando la propiedad **SoundEffects** devuelve **true**, se reproducirán los efectos de sonido incluidos en la definición de un carácter. Si **es false**, los efectos sonoros no se reproducirán. El valor de la propiedad afecta a todos los caracteres y es de solo lectura; solo el usuario puede establecer este valor de propiedad.

## <a name="see-also"></a>Consulte también

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




