---
title: Notas del método Visual Basic accName
description: El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903526"
---
# <a name="visual-basic-method-notes-accname"></a><span data-ttu-id="f5db8-103">Notas del método Visual Basic: accName</span><span class="sxs-lookup"><span data-stu-id="f5db8-103">Visual Basic Method Notes: accName</span></span>

<span data-ttu-id="f5db8-104">El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++.</span><span class="sxs-lookup"><span data-stu-id="f5db8-104">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="f5db8-105">El archivo oleacc. ODL contiene la siguiente definición para la versión que establece la propiedad de la función:</span><span class="sxs-lookup"><span data-stu-id="f5db8-105">The file Oleacc.odl contains the following definition for the version that sets the property of the function:</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



<span data-ttu-id="f5db8-106">Aunque el parámetro *varChild* se muestra como opcional en el archivo ODL y en el examinador de objetos, debe incluirlo al llamar a la versión de configuración de propiedad de [**accName**](https://www.bing.com/search?q=**accName**).</span><span class="sxs-lookup"><span data-stu-id="f5db8-106">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accName**](https://www.bing.com/search?q=**accName**).</span></span>

 

 




