---
title: Cadenas de formato de procedimiento
description: La siguiente es una descripción completa de la cadena de formato. Ensambla todas las capas relacionadas con diferentes fases de la evolución del intérprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995490"
---
# <a name="procedure-format-strings"></a>Cadenas de formato de procedimiento

La siguiente es una descripción completa de la cadena de formato. Ensambla todas las capas relacionadas con diferentes fases de la evolución del intérprete.

## <a name="procedure-descriptor-overview"></a>Introducción a los descriptores de procedimientos

Un descriptor de procedimiento consta de los descriptores de encabezado y los descriptores de parámetros. La descripción del estilo [**– OI**](/windows/desktop/Midl/-oi) se considera obsoleta, en términos de uso común en la programación RPC actual. **: Los salientes** se consideran más actuales.

## <a name="the-oi-style-description"></a>La descripción del estilo – OI

Esta descripción consta de lo siguiente:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

El encabezado tendría de 6 a 16 bytes.

La descripción completa se genera al compilar en el modo [**OI**](/windows/desktop/Midl/-oi) . En el modo [**– os**](/windows/desktop/Midl/-os) , solo se generan los descriptores de parámetro, que se usan para la conversión. El intérprete de selección usa descriptores de parámetros de estilo antiguos.

## <a name="the-oif-style-description"></a>La descripción del estilo – salientes

La descripción consta de lo siguiente:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

El descriptor de encabezado de estilo [**–FUL**](/windows/desktop/Midl/-oi) está compuesto por

La descripción del estilo – interfaces se genera al compilar en el modo [**-**](/windows/desktop/Midl/-oi) transformated o **– Oicf** del compilador.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Algunas características más recientes como canalización, Async y [**/Robust**](/windows/desktop/Midl/-robust) fuerzan el modo [**– Oicf**](/windows/desktop/Midl/-oi) del compilador cuando se usan.

## <a name="the-extended-oif-description"></a>Descripción extendida – interfaces

La descripción consta de lo siguiente:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 