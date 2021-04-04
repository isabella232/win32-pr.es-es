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
# <a name="visual-basic-method-notes-accvalue"></a>Notas del método Visual Basic: accValue

El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++. El archivo oleacc. ODL contiene la siguiente definición para la versión que establece la propiedad de la función.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Aunque el parámetro *varChild* se muestra como opcional en el archivo ODL y en el examinador de objetos, debe incluirlo al llamar a la versión de configuración de propiedad de [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




