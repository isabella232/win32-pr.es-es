---
title: Cadenas de formato de procedimiento
description: A continuación se muestra una descripción completa de la cadena de formato. Ensambla todas las capas relacionadas con las distintas fases de la evolución del intérprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019063"
---
# <a name="procedure-format-strings"></a>Cadenas de formato de procedimiento

A continuación se muestra una descripción completa de la cadena de formato. Ensambla todas las capas relacionadas con las distintas fases de la evolución del intérprete.

## <a name="procedure-descriptor-overview"></a>Información general sobre el descriptor de procedimientos

Un descriptor de procedimiento consta de los descriptores de encabezado y los descriptores de parámetros. La [**descripción del estilo –Oi**](/windows/desktop/Midl/-oi) se considera obsoleta, en términos de uso común en la programación RPC actual. **–Oif se** considera más actual.

## <a name="the-oi-style-description"></a>Descripción del estilo –Oi

Esta descripción consta de lo siguiente:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

El encabezado tendría entre 6 y 16 bytes.

La descripción completa se genera al compilar en [**modo –Oi.**](/windows/desktop/Midl/-oi) En [**el modo –Os,**](/windows/desktop/Midl/-os) solo se generan los descriptores de parámetros, que se usan para la conversión. El intérprete de selección usa descriptores de parámetros de estilo antiguos.

## <a name="the-oif-style-description"></a>Descripción del estilo –Oif

La descripción consta de lo siguiente:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

El descriptor de encabezado de estilo [**–Oif**](/windows/desktop/Midl/-oi) consta de

La descripción del estilo –Oif se genera al compilar en el modo [**–Oif**](/windows/desktop/Midl/-oi) o **–Oicf** del compilador.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Algunas características más recientes, como pipe, async y [**/robust,**](/windows/desktop/Midl/-robust) fuerzan el modo [**–Oicf**](/windows/desktop/Midl/-oi) del compilador, cuando se usa.

## <a name="the-extended-oif-description"></a>La descripción extendida de –Oif

La descripción consta de lo siguiente:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 