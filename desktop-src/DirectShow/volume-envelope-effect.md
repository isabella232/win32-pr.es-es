---
description: Efecto de sobre de volumen
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efecto de sobre de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ecb66914063596849522a0e4bb340fc84f7d80e5ea1113bfdae2d32e855d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746955"
---
# <a name="volume-envelope-effect"></a>Efecto de sobre de volumen

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El efecto Sobre de volumen establece el volumen en una secuencia de audio.

Identificador de clase (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nombre de la variable CLSID: CLSID \_ AudMixer

Propiedades



| Propiedad | Tipo   | Valor predeterminado | Descripción                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | Volumen, como porcentaje del volumen autor. Puede generar atenuaciones de audio si varía este valor de propiedad con el tiempo. |



 

## <a name="remarks"></a>Comentarios

Cada objeto de una escala de tiempo puede tener como máximo un efecto de sobre de volumen. En una composición o un grupo, el sobre de volumen se aplica primero, antes que cualquier otro efecto de audio, independientemente de su prioridad. En un origen o una pista, el efecto del volumen se aplica según su prioridad.

 

 



