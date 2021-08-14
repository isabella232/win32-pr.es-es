---
title: Obtención de interfaces ADSI de la extensión
description: Una extensión a menudo necesita obtener datos del objeto de directorio al que se enlaza.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, obtener interfaces ADSI de la extensión
- ADSI ADSI, código de ejemplo C/C++, obtención de interfaces ADSI de la extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41df2498bd0c25996cfd0941f823e414289c0a9fbe006df846960c6f455e4301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179735"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Obtención de interfaces ADSI de la extensión

Una extensión a menudo necesita obtener datos del objeto de directorio al que se enlaza. Por ejemplo, una extensión para un **objeto de** equipo puede querer obtener el **dnsHostName** del objeto actual del directorio. Esto se puede lograr fácilmente mediante la emisión de una llamada **QueryInterface** en la [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el agregador.


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



Debe liberar la interfaz inmediatamente después de su uso. Si la extensión tiene una referencia abierta al agregador, ha creado una referencia circular y el agregador no puede liberar la extensión. Por lo tanto, no se puede liberar el agregador y el resultado son pérdidas de memoria en la aplicación.

 

 