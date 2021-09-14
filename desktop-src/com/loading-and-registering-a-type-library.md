---
title: Cargar y registrar una biblioteca de tipos
description: La biblioteca de vínculos dinámicos de Automation, Oleaut32.dll, proporciona varias funciones a las que puede llamar para cargar y registrar una biblioteca de tipos. Al llamar a LoadTypeLibEx, como se muestra en el ejemplo siguiente, se carga la biblioteca y se crean las entradas del Registro.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d533225913d6bcfbb74df3ac42bd00b18b00e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249267"
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

 

 