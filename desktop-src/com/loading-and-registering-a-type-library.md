---
title: Cargar y registrar una biblioteca de tipos
description: La biblioteca de vínculos dinámicos de Automation, Oleaut32.dll, proporciona varias funciones a las que puede llamar para cargar y registrar una biblioteca de tipos. Al llamar a LoadTypeLibEx, como se muestra en el ejemplo siguiente, se carga la biblioteca y se crean las entradas del Registro.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854235"
---
# <a name="loading-and-registering-a-type-library"></a>Cargar y registrar una biblioteca de tipos

La biblioteca de vínculos dinámicos de Automation, Oleaut32.dll, proporciona varias funciones a las que puede llamar para cargar y registrar una biblioteca de tipos. Al [llamar a LoadTypeLibEx](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), como se muestra en el ejemplo siguiente, carga la biblioteca y crea las entradas del Registro.

## <a name="example"></a>Ejemplo

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

 

 