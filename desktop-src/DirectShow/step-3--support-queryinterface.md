---
description: Exponga las nuevas interfaces de un filtro a los clientes como parte de la creación de una página de propiedades de filtro para un filtro directShow personalizado.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Paso 3. Compatibilidad con QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410028"
---
# <a name="step-3-support-queryinterface"></a>Paso 3. Compatibilidad con QueryInterface

Para exponer las nuevas interfaces del filtro a los clientes, haga lo siguiente:

-   Incluya la [**macro DECLARE \_ IUNKNOWN en**](declare-iunknown.md) la sección de declaración pública del filtro:
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Invalide [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) para comprobar los IID de las dos interfaces:
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

Siguiente: [Paso 4. Cree la página de propiedades](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una página de propiedades de filtro](creating-a-filter-property-page.md)
</dt> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



