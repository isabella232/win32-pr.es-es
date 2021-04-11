---
description: Matriz de plantillas de fábrica
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matriz de plantillas de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152695"
---
# <a name="factory-template-array"></a>Matriz de plantillas de fábrica

La plantilla de generador contiene las siguientes variables de miembro público:

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

La primera es la función de creación de instancias del componente. La segunda es una función de inicialización opcional. Si se proporciona una función de inicialización, se llama desde dentro de la función de punto de entrada del archivo DLL. (La función de punto de entrada de DLL se describe más adelante en este artículo).

Supongamos que está creando un archivo DLL que contiene un componente denominado CMyComponent, que hereda de [**CUnknown**](cunknown.md). Debe proporcionar los elementos siguientes en el archivo DLL:

-   La función de inicialización, un método público que devuelve una nueva instancia de CMyComponent.
-   Una matriz global de plantillas de fábrica, denominada *g \_ templates.* Esta matriz contiene la plantilla de generador para CMyComponent.
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



El `CreateInstance` método llama al constructor de clase y devuelve un puntero a la nueva instancia de clase. El parámetro *pUnk* es un puntero al [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)de agregación. Simplemente puede pasar este parámetro al constructor de clase. El parámetro *pHr* es un puntero a un valor HRESULT. El constructor de clase establece este en un valor adecuado, pero si se produce un error en el constructor, establezca el valor en E \_ OUTOFMEMORY.

La macro [**Name**](name.md) genera una cadena en las compilaciones de depuración, pero se resuelve como **null** en las compilaciones comerciales. Se usa en este ejemplo para dar al componente un nombre que aparece en los registros de depuración, pero no ocupa la memoria en la versión final.

El `CreateInstance` método puede tener cualquier nombre, ya que el generador de clases hace referencia al puntero de función en la plantilla de generador. Sin embargo, *g \_ templates* y *g \_ cTemplates* son variables globales que el generador de clases espera encontrar, por lo que deben tener exactamente esos nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un archivo DLL de filtro de DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
