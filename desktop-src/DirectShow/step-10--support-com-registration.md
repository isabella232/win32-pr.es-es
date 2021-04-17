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
# <a name="step-10-support-com-registration"></a><span data-ttu-id="01a18-104">Paso 10.</span><span class="sxs-lookup"><span data-stu-id="01a18-104">Step 10.</span></span> <span data-ttu-id="01a18-105">Compatibilidad con el registro COM</span><span class="sxs-lookup"><span data-stu-id="01a18-105">Support COM Registration</span></span>

<span data-ttu-id="01a18-106">La última tarea restante es admitir el registro COM, por lo que el marco de propiedades puede crear nuevas instancias de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="01a18-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="01a18-107">Agregue otra entrada [**CFactoryTemplate**](cfactorytemplate.md) a la matriz global *g \_ templates* , que se usa para registrar todos los objetos com en el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="01a18-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="01a18-108">No incluya ninguna información de configuración de filtro para la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="01a18-108">Do not include any filter set-up information for the property page.</span></span>


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



<span data-ttu-id="01a18-109">Si declara *g \_ cTemplates* como se muestra en el código siguiente, el valor correcto se basa automáticamente en el tamaño de la matriz:</span><span class="sxs-lookup"><span data-stu-id="01a18-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="01a18-110">Además, agregue un `CreateInstance` método estático a la clase de página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="01a18-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="01a18-111">Puede asignar el nombre que prefiera al método, pero la firma debe coincidir con la que se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="01a18-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


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



<span data-ttu-id="01a18-112">Para probar la página de propiedades, registre el archivo DLL y, a continuación, cargue el filtro en GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="01a18-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="01a18-113">Haga clic con el botón secundario en el filtro y seleccione **propiedades del filtro**.</span><span class="sxs-lookup"><span data-stu-id="01a18-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01a18-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01a18-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a18-115">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="01a18-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="01a18-116">Cómo crear un archivo DLL de filtro de DirectShow</span><span class="sxs-lookup"><span data-stu-id="01a18-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



