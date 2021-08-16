---
description: Matriz de plantillas de fábrica
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matriz de plantillas de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1888a2a054473865c713d96cdfa5706c35229dc938f23513a95066176ab138c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401850"
---
# <a name="factory-template-array"></a>Matriz de plantillas de fábrica

La plantilla de generador contiene las siguientes variables miembro públicas:

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Los dos punteros de función, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) y [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usan las siguientes definiciones de tipo:

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

La primera es la función de creación de instancias para el componente. La segunda es una función de inicialización opcional. Si proporciona una función de inicialización, se llama desde dentro de la función de punto de entrada de DLL. (La función de punto de entrada de DLL se describe más adelante en este artículo).

Supongamos que está creando un archivo DLL que contiene un componente denominado CMyComponent, que hereda de [**CUnknown**](cunknown.md). Debe proporcionar los siguientes elementos en el archivo DLL:

-   Función de inicialización, un método público que devuelve una nueva instancia de CMyComponent.
-   Una matriz global de plantillas de generador, denominada *g \_ Templates.* Esta matriz contiene la plantilla de generador para CMyComponent.
-   Una variable global denominada *g \_ cTemplates* que especifica el tamaño de la matriz.

En el ejemplo siguiente se muestra cómo declarar estos elementos:


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



El `CreateInstance` método llama al constructor de clase y devuelve un puntero a la nueva instancia de clase. El parámetro *pUnk* es un puntero al [**IUnknown que**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)agrega . Simplemente puede pasar este parámetro al constructor de clase. El parámetro *pHr* es un puntero a un valor HRESULT. El constructor de clase establece esto en un valor adecuado, pero si se produce un error en el constructor, establezca el valor en E \_ OUTOFMEMORY.

La [**macro NAME**](name.md) genera una cadena en las compilaciones de depuración, pero se resuelve como NULL **en** las compilaciones comerciales. Se usa en este ejemplo para dar al componente un nombre que aparece en los registros de depuración, pero que no ocupa memoria en la versión final.

El `CreateInstance` método puede tener cualquier nombre, porque el generador de clases hace referencia al puntero de función en la plantilla de generador. Sin embargo, *g \_ Templates* y *g \_ cTemplates* son variables globales que el generador de clases espera encontrar, por lo que deben tener exactamente esos nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un archivo DIRECTSHOW DLL de filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 
