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
# <a name="visual-basic-method-notes-accname"></a>Notas del método Visual Basic: accName

El archivo de lenguaje de descripción de objetos (ODL), oleacc. ODL, contiene información que difiere de la implementación de C/C++. El archivo oleacc. ODL contiene la siguiente definición para la versión que establece la propiedad de la función:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Aunque el parámetro *varChild* se muestra como opcional en el archivo ODL y en el examinador de objetos, debe incluirlo al llamar a la versión de configuración de propiedad de [**accName**](https://www.bing.com/search?q=**accName**).

 

 




