---
title: Llamadas a funciones
description: Llamadas a funciones
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Reproductor de Windows Media máscaras, llamar a funciones en JScript
- máscaras, llamar a funciones en JScript
- llamar a funciones en JScript
- JScript para máscaras, funciones de llamada
- Reproductor de Windows Media máscaras,atributo scriptFile en JScript
- atributo skins,scriptFile en JScript
- attributes,scriptFile en JScript
- Atributo scriptFile en JScript
- JScript archivos para máscaras,atributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764275"
---
# <a name="calling-functions"></a>Llamadas a funciones

Si necesita llamar a más de unas pocas líneas de código, puede cargar un archivo de script mediante el atributo **scriptFile** del elemento **VIEW** y llamar a las funciones del script. Puede cargar más de un archivo por vista:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Una vez cargados los archivos de script, puede llamar a funciones en ellos desde la sección Vista. Por ejemplo, para llamar a una función denominada *myfunction* cuando se hace clic en algo, escriba lo siguiente:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Si tiene más de una vista, solo las funciones de los archivos cargados en la vista actual están disponibles para xml y JScript código que se ejecuta con la vista actual. Los archivos cargados en otras vistas no están en el ámbito de la vista actual.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de JScript**](using-jscript.md)
</dt> </dl>

 

 




