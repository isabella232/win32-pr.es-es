---
description: Paso 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Paso 10. Compatibilidad con el registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678087"
---
# <a name="step-10-support-com-registration"></a>Paso 10. Compatibilidad con el registro COM

La última tarea restante es admitir el registro COM, por lo que el marco de propiedades puede crear nuevas instancias de la página de propiedades. Agregue otra entrada [**CFactoryTemplate**](cfactorytemplate.md) a la matriz global *g \_ templates* , que se usa para registrar todos los objetos com en el archivo dll. No incluya ninguna información de configuración de filtro para la página de propiedades.


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



Si declara *g \_ cTemplates* como se muestra en el código siguiente, el valor correcto se basa automáticamente en el tamaño de la matriz:


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Además, agregue un `CreateInstance` método estático a la clase de página de propiedades. Puede asignar el nombre que prefiera al método, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:


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



Para probar la página de propiedades, registre el archivo DLL y, a continuación, cargue el filtro en GraphEdit. Haga clic con el botón secundario en el filtro y seleccione **propiedades del filtro**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Cómo crear un archivo DLL de filtro de DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 



