---
description: Las devoluciones de llamada de los componentes hospedados son lo que hace posible el hospedaje. Sin embargo, es posible que el componente que hospeda haya activado otro contexto de activación que usa para acceder a complementos o componentes propios.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Usar devoluciones de llamada de componentes hospedados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884605"
---
# <a name="using-callbacks-from-hosted-components"></a>Usar devoluciones de llamada de componentes hospedados

Las devoluciones de llamada de los componentes hospedados son lo que hace posible el hospedaje. Sin embargo, es posible que el componente que hospeda haya activado otro contexto de activación que usa para acceder a complementos o componentes propios. En este caso, si el componente hospedado deja un contexto de activación en la pila que hace referencia a su propio objeto COM, la aplicación de hospedaje podría llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto que espera que sea su propia implementación y, en su lugar, recibir el objeto del componente hospedado. Para evitar esta herencia de contextos de activación, una buena aplicación de hospedaje debe activar primero su propio contexto de activación conocido durante una devolución de llamada.

Considere el ejemplo siguiente que protege el código de la aplicación de hospedaje:

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

Esto garantiza que se establece un contexto de activación adecuado antes de pasar la solicitud a alguna implementación interna de **Funct**. Su propia implementación puede tener la implementación real insertada, pero el método anterior garantiza una interoperabilidad más sencilla mediante la creación de contenedores delegados. Se recomienda usar un método similar al exponer devoluciones de llamada normales (no COM).

 

 
