---
title: Uso de IADsExtension
description: Este tema contiene ejemplos de código de C++ para usar la interfaz IADsExtension.
ms.assetid: 56bc87b4-f3cf-4177-90cb-e745889f8fef
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a844d320b28548e9e9998881fd2a09815d1882e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268258"
---
# <a name="iadsextension-usage"></a>Uso de IADsExtension

[**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) es una interfaz opcional implementada por el escritor de la extensión cuando se cumple al menos una de las siguientes condiciones:

-   El componente de extensión requiere una notificación de inicialización, tal y como se define en **ADSI \_ ext \_ * dwCode*** en el método [**Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) .
-   La extensión admite una interfaz dual o de distribución.

Si un componente de extensión admite la interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) por primera razón, los métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y [**IADsExtension::P rivateinvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) pueden devolver **E \_ NOTIMPL**. Como alternativa, si un componente de extensión admite una interfaz dual o de distribución, el método de [**operación**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) puede omitir los datos y devolver un **valor HRESULT** de **E \_ NOTIMPL**.

En el código siguiente se muestra una extensión que implementa [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).


```C++
STDMETHOD(Operate)(ULONG dwCode, VARIANT varData1, VARIANT varData2, VARIANT varData3)
{
    HRESULT hr = S_OK;
    switch (dwCode) 
    {
    case ADS_EXT_INIT:
         // Prompt for a credential.
         // MessageBox(NULL, "INITCRED", "ADsExt", MB_OK);
          break;
    default:
          hr = E_FAIL;
          break;
    }        
    return hr;        
}
 
STDMETHOD(PrivateGetIDsOfNames)(REFIID riid, OLECHAR ** rgszNames, unsigned int cNames, LCID lcid, DISPID  * rgdispid)
{        
      if (rgdispid == NULL)
      {
        return E_POINTER;
      }    
    return  DispGetIDsOfNames(m_pTypeInfo, rgszNames, cNames, rgdispid);
}
 
STDMETHOD(PrivateInvoke)(DISPID dispidMember, REFIID riid, LCID lcid, WORD wFlags, DISPPARAMS * pdispparams, VARIANT * pvarResult, EXCEPINFO * pexcepinfo, UINT * puArgErr)
{
 return DispInvoke( (IHelloWorld*)this, 
           m_pTypeInfo,
        dispidMember, 
        wFlags, 
        pdispparams, 
        pvarResult, 
        pexcepinfo, 
        puArgErr );
}
```



 

 




