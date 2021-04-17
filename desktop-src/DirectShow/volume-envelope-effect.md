---
description: Efecto sobre volumen
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efecto sobre volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687862"
---
# <a name="volume-envelope-effect"></a>Efecto sobre volumen

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El efecto sobre volumen establece el volumen en una secuencia de audio.

IDENTIFICADOR de clase (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nombre de la variable CLSID: CLSID \_ AudMixer

Propiedades



| Propiedad | Tipo   | Valor predeterminado | Descripción                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1,0     | Volumen, como porcentaje del volumen creado. Puede producir fundidos de audio modificando este valor de propiedad a lo largo del tiempo. |



 

## <a name="remarks"></a>Observaciones

Cada objeto de una escala de tiempo puede tener como máximo un efecto de sobre de volumen. En una composición o un grupo, el sobre del volumen se aplica primero, antes que cualquier otro efecto de audio, independientemente de su prioridad. En un origen o una pista, el efecto de volumen se aplica en función de su prioridad.

 

 



