---
description: Una aplicación debe usar una estructura RECT para definir un rectángulo.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordenadas del rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997317"
---
# <a name="rectangle-coordinates"></a>Coordenadas del rectángulo

Una aplicación debe usar una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para definir un rectángulo. La estructura especifica las coordenadas de dos puntos: las esquinas superior izquierda e inferior derecha del rectángulo. Los lados del rectángulo se extienden desde estos dos puntos y son paralelos a los ejes x e y.

Los valores de las coordenadas de un rectángulo se expresan como enteros con signo. El valor de la coordenada del lado derecho de un rectángulo debe ser mayor que el del lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

Dado que las aplicaciones pueden usar rectángulos para muchos fines diferentes, las funciones de rectángulo no usan una unidad de medida explícita. En su lugar, todas las coordenadas y dimensiones del rectángulo se proporcionan en valores lógicos con signo. El modo de asignación y la función en la que se utiliza el rectángulo determinan las unidades de medida. Para obtener más información sobre las coordenadas y los modos de asignación, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).

 

 
