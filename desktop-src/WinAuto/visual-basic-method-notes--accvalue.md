---
title: Notas del método Visual Basic accValue
description: El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++. El archivo oleacc. ODL contiene la siguiente definición para la versión que establece la propiedad de la función.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075571"
---
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="b9432-104">Notas del método Visual Basic: accValue</span><span class="sxs-lookup"><span data-stu-id="b9432-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="b9432-105">El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++.</span><span class="sxs-lookup"><span data-stu-id="b9432-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="b9432-106">El archivo oleacc. ODL contiene la siguiente definición para la versión que establece la propiedad de la función.</span><span class="sxs-lookup"><span data-stu-id="b9432-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="b9432-107">Aunque el parámetro *varChild* se muestra como opcional en el archivo ODL y en el examinador de objetos, debe incluirlo al llamar a la versión de configuración de propiedad de [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span><span class="sxs-lookup"><span data-stu-id="b9432-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




