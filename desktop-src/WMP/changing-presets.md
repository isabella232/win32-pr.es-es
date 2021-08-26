---
title: Cambiar valores preestablecidos
description: Cambiar valores preestablecidos
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizaciones, ejemplo de efecto de efecto
- visualizaciones personalizadas, ejemplo de efecto de efecto
- guía de programación, visualizaciones
- samples,Visualizaciones de efecto de sonido
- Ejemplo de visualización de efecto de efecto de efecto de efecto
- visualizaciones, valores preestablecidos
- visualizaciones personalizadas, valores preestablecidos
- presets in visualizations,Glow sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863915"
---
# <a name="changing-presets"></a>Cambiar valores preestablecidos

Se han cambiado las siguientes secciones de código preestablecido para permitir tres valores preestablecidos:

## <a name="getpresettitle"></a>GetPresetTitle

Este código se insertó en lugar del código preestablecido generado:


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Enumeraciones

La enumeración siguiente de Glow.h se cambió para permitir tres valores preestablecidos:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Encabezado de recurso

Los siguientes recursos se definieron en Resource.h para permitir tres valores preestablecidos:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Tenga en cuenta que también debe cambiar el número de recursos **\_ de APS NEXT \_ \_ SYMED \_ VALUE** a 106.

## <a name="resource-file"></a>Archivo de recursos

Las cadenas siguientes deben cambiarse en el archivo Glowdll.rc para permitir tres valores preestablecidos y darles nombres:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de efecto de efecto de efecto de efecto**](the-glow-sample.md)
</dt> </dl>

 

 




