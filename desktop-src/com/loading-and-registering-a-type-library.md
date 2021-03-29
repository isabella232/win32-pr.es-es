---
title: Cargar y registrar una biblioteca de tipos
description: La biblioteca de vínculos dinámicos de Automation, Oleaut32.dll, proporciona varias funciones que se pueden llamar para cargar y registrar una biblioteca de tipos. La llamada a LoadTypeLibEx, como se muestra en el ejemplo siguiente, carga la biblioteca y crea las entradas del registro.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078484"
---
# <a name="loading-and-registering-a-type-library"></a><span data-ttu-id="12076-104">Cargar y registrar una biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="12076-104">Loading and Registering a Type Library</span></span>

<span data-ttu-id="12076-105">La biblioteca de vínculos dinámicos de Automation, Oleaut32.dll, proporciona varias funciones que se pueden llamar para cargar y registrar una biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="12076-105">The Automation dynamic link library, Oleaut32.dll, provides several functions that you can call to load and register a type library.</span></span> <span data-ttu-id="12076-106">La llamada a [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), como se muestra en el ejemplo siguiente, carga la biblioteca y crea las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="12076-106">Calling [LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), as shown in the following example, both loads the library and creates the registry entries.</span></span>

## <a name="example"></a><span data-ttu-id="12076-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12076-107">Example</span></span>

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 