---
title: Propiedad SoundEffectsOn
description: Propiedad SoundEffectsOn
ms.assetid: 478c4748-5ca1-4237-958a-17f0a476c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664a9f3ce4e76d7f42cc6fb15e737bea302730bb03ea414e968336ee147772cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975715"
---
# <a name="soundeffectson-property"></a>Propiedad SoundEffectsOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si los efectos de sonido están habilitados para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agente*. **Characters("**_CharacterID_*_"). SoundEffectsOn_* \[  =  *boolean*\]



| Parte      | Descripción                                                                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si se habilitan los efectos de sonido. **True** Los efectos de sonido están habilitados.<br/> **False** Los efectos de sonido están deshabilitados.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad determina si los efectos de sonido incluidos como parte de las animaciones de un carácter se reproducirán cuando se reproduce una animación. La configuración de esta propiedad se aplica a todos los clientes del carácter.

## <a name="see-also"></a>Consulte también

[**Propiedad SoundEffects**](soundeffects-property.md)


 

 





