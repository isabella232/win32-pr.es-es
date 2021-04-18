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
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="fe1f0-105">Obtención de interfaces ADSI de la extensión</span><span class="sxs-lookup"><span data-stu-id="fe1f0-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="fe1f0-106">A menudo, una extensión necesita obtener datos del objeto de directorio al que se enlaza.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="fe1f0-107">Por ejemplo, una extensión de un objeto de **equipo** puede querer obtener el **DnsHostName** del objeto actual desde el directorio.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="fe1f0-108">Esto se puede lograr fácilmente emitiendo una llamada **QueryInterface** en la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para el agregador.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


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



<span data-ttu-id="fe1f0-109">Debe liberar la interfaz inmediatamente después de usarla.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="fe1f0-110">Si la extensión tiene una referencia abierta al agregador, se ha creado una referencia circular y el agregador no puede liberar la extensión.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="fe1f0-111">Por lo tanto, no se puede liberar el agregador y el resultado son fugas de memoria en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 