---
title: Visual Basic Notas del método accValue
description: El archivo del lenguaje de descripción de objetos (ODL), Oleacc.odl, contiene información que difiere de la implementación de C/C++. El archivo Oleacc.odl contiene la siguiente definición para la versión que establece la propiedad de la función.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744785"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Notas del método: accValue

El archivo del lenguaje de descripción de objetos (ODL), Oleacc.odl, contiene información que difiere de la implementación de C/C++. El archivo Oleacc.odl contiene la siguiente definición para la versión que establece la propiedad de la función.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Aunque el *parámetro varChild aparece* como opcional en el archivo ODL y el explorador de objetos, debe incluirlo al llamar a la versión de configuración de propiedades [**de accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




