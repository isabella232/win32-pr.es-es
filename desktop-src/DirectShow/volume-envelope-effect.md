---
description: Efecto de sobre de volumen
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Efecto de sobre de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272759"
---
# <a name="volume-envelope-effect"></a>Efecto de sobre de volumen

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El efecto Sobre de volumen establece el volumen en una secuencia de audio.

Id. de clase (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}

Nombre de la variable CLSID: CLSID \_ AudMixer

Propiedades



| Propiedad | Tipo   | Valor predeterminado | Descripción                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | Volumen, como porcentaje del volumen autor. Puede generar atenuaciones de audio si varía este valor de propiedad con el tiempo. |



 

## <a name="remarks"></a>Observaciones

Cada objeto de una escala de tiempo puede tener como máximo un efecto de sobre de volumen. En una composición o un grupo, el sobre de volumen se aplica primero, antes que cualquier otro efecto de audio, independientemente de su prioridad. En un origen o una pista, el efecto del volumen se aplica según su prioridad.

 

 



