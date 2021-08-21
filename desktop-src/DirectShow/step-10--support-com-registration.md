---
description: Paso 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Paso 10. Compatibilidad con el registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68efdeda754d5f7b728138a26a6bc9f4b782918f8c4b5140fd2457bcee6012f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652155"
---
# <a name="step-10-support-com-registration"></a>Paso 10. Compatibilidad con el registro COM

La última tarea restante consiste en admitir el registro COM, para que el marco de propiedades pueda crear nuevas instancias de la página de propiedades. Agregue otra [**entrada CFactoryTemplate**](cfactorytemplate.md) a la matriz *global g \_ Templates,* que se usa para registrar todos los objetos COM en el archivo DLL. No incluya información de configuración de filtro para la página de propiedades.


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



Si declara *g \_ cTemplates* como se muestra en el código siguiente, tiene automáticamente el valor correcto en función del tamaño de la matriz:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Además, agregue un método estático a `CreateInstance` la clase de página de propiedades. Puede dar al método el nombre que prefiera, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



Para probar la página de propiedades, registre el archivo DLL y, a continuación, cargue el filtro en GraphEdit. Haga clic con el botón derecho en el filtro y seleccione **Filtrar propiedades.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Cómo crear un archivo DLL DirectShow filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 



