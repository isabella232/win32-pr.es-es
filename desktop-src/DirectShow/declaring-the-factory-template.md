---
description: Declaración de la plantilla de fábrica
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Declaración de la plantilla de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71a925df01eee1f6e8c4365de4f00afd32b3449aa6ee07bc949e225713c2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953194"
---
# <a name="declaring-the-factory-template"></a>Declaración de la plantilla de fábrica

El siguiente paso consiste en declarar la plantilla de generador para el filtro. Una plantilla de generador es una clase de C++ que contiene información para el generador de clases. En el archivo DLL, declare una matriz global de [**objetos CFactoryTemplate,**](cfactorytemplate.md) una para cada filtro o componente COM del archivo DLL. La matriz debe denominarse *g \_ Templates*. Para obtener más información sobre las plantillas de generador, [vea How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).

El **miembro m \_ pAMovieSetup \_ Filter** de la plantilla de generador es un puntero a la estructura FILTER de [**AMOVIESETUP \_**](amoviesetup-filter.md) descrita anteriormente. En el ejemplo siguiente se muestra una plantilla de generador con la estructura que se ha dado en el ejemplo anterior:


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



Si no ha declarado ninguna información de filtro, **m \_ pAMoveSetup \_ Filter** puede ser **NULL.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de filtros DirectShow filtros](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



