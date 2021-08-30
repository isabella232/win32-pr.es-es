---
description: Una aplicación debe usar una estructura RECT para definir un rectángulo.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordenadas del rectángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf39ba5676b56fc3b9a32fbdd002944955d9e977e93eb4a7943c8a07be75946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092795"
---
# <a name="rectangle-coordinates"></a>Coordenadas del rectángulo

Una aplicación debe usar una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) para definir un rectángulo. La estructura especifica las coordenadas de dos puntos: las esquinas superior izquierda e inferior derecha del rectángulo. Los lados del rectángulo se extienden desde estos dos puntos y son paralelos al eje X y al eje Y.

Los valores de coordenadas de un rectángulo se expresan como enteros con signo. El valor de la coordenada del lado derecho de un rectángulo debe ser mayor que el de su lado izquierdo. Del mismo modo, el valor de la coordenada de la parte inferior debe ser mayor que el de la parte superior.

Dado que las aplicaciones pueden usar rectángulos para muchos propósitos diferentes, las funciones de rectángulo no usan una unidad de medida explícita. En su lugar, todas las coordenadas y dimensiones del rectángulo se dan en valores lógicos con firma. El modo de asignación y la función en la que se usa el rectángulo determinan las unidades de medida. Para obtener más información sobre las coordenadas y los modos de asignación, vea [Espacios de coordenadas y transformaciones.](coordinate-spaces-and-transformations.md)

 

 
