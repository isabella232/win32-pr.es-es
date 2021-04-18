---
title: Obtención de interfaces ADSI de la extensión
description: A menudo, una extensión necesita obtener datos del objeto de directorio al que se enlaza.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- extensiones ADSI, obtener interfaces ADSI de la extensión
- ADSI ADSI, código de ejemplo C/C++, obtener interfaces ADSI de la extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656419"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Obtención de interfaces ADSI de la extensión

A menudo, una extensión necesita obtener datos del objeto de directorio al que se enlaza. Por ejemplo, una extensión de un objeto de **equipo** puede querer obtener el **DnsHostName** del objeto actual desde el directorio. Esto se puede lograr fácilmente emitiendo una llamada **QueryInterface** en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el agregador.


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



Debe liberar la interfaz inmediatamente después de usarla. Si la extensión tiene una referencia abierta al agregador, se ha creado una referencia circular y el agregador no puede liberar la extensión. Por lo tanto, no se puede liberar el agregador y el resultado son fugas de memoria en la aplicación.

 

 