---
description: Declaración de la plantilla de fábrica
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Declaración de la plantilla de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152060"
---
# <a name="declaring-the-factory-template"></a>Declaración de la plantilla de fábrica

El siguiente paso consiste en declarar la plantilla de generador para el filtro. Una plantilla de generador es una clase de C++ que contiene información para el generador de clases. En el archivo DLL, declare una matriz global de objetos [**CFactoryTemplate**](cfactorytemplate.md) , uno para cada filtro o componente com del archivo dll. La matriz se debe denominar *g \_ templates*. Para obtener más información acerca de las plantillas de fábrica, consulte [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).

El miembro de **\_ \_ filtro m pAMovieSetup** de la plantilla de generador es un puntero a la estructura de [**\_ filtros AMOVIESETUP**](amoviesetup-filter.md) descrita anteriormente. En el ejemplo siguiente se muestra una plantilla de generador, usando la estructura proporcionada en el ejemplo anterior:


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



Si no declaras ninguna información de filtro, el **\_ \_ filtro m PAMoveSetup** puede ser **null**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



