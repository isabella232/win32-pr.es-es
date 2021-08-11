---
title: Propiedad SoundEffects
description: Propiedad SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3894782ec3a038831f7bab7d6d5fe0701936baf1c1add136ad5c2c3446f78867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246261"
---
# <a name="soundeffects-property"></a>Propiedad SoundEffects

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor booleano que indica si los efectos de sonido (. Wav) se reproducirán los archivos configurados como parte de las acciones de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent!". AudioOutput.SoundEffects**



| Valor     | Descripción                          |
|-----------|--------------------------------------|
| **True**  | Los efectos de sonido de caracteres están habilitados. |
| **False** | El efecto de sonido de caracteres está deshabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad refleja la opción Reproducir efectos de sonido de caracteres en la página Salida de la hoja de propiedades agente (Opciones avanzadas de caracteres). Cuando la **propiedad SoundEffects** devuelve **True,** se reproducirán los efectos de sonido incluidos en la definición de un carácter. Cuando **es False,** no se reproducirán los efectos de sonido. El valor de propiedad afecta a todos los caracteres y es de solo lectura; solo el usuario puede establecer este valor de propiedad.

## <a name="see-also"></a>Consulte también

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




