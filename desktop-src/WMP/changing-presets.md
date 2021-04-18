---
title: Cambiar valores preestablecidos
description: Cambiar valores preestablecidos
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualizaciones, muestra brillante
- visualizaciones personalizadas, ejemplo de resplandor
- Guía de programación, visualizaciones
- ejemplos, visualización de resplandor
- Ejemplo de visualización brillante
- visualizaciones, valores preestablecidos
- visualizaciones personalizadas, valores preestablecidos
- valores preestablecidos en visualizaciones, muestra brillante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695308"
---
# <a name="changing-presets"></a>Cambiar valores preestablecidos

Se cambiaron las siguientes secciones de código preestablecidas para permitir tres valores preestablecidos:

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

La siguiente enumeración en Glow. h se cambió para permitir tres valores preestablecidos:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Encabezado de recurso

Los siguientes recursos se definieron en Resource. h para permitir tres valores preestablecidos:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Tenga en cuenta que también debe cambiar el número de recurso de **\_ APS \_ Next \_ SYMED \_ Value** por 106.

## <a name="resource-file"></a>Archivo de recursos

Las cadenas siguientes deben cambiarse en el archivo Glowdll. RC para permitir tres valores preestablecidos y asignarles nombres:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de resplandor**](the-glow-sample.md)
</dt> </dl>

 

 




