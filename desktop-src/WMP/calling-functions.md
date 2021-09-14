---
title: Llamadas a funciones
description: Llamadas a funciones
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Reproductor de Windows Media máscaras, llamar a funciones en JScript
- máscaras, llamar a funciones en JScript
- llamar a funciones en JScript
- JScript archivos para máscaras, funciones de llamada
- Reproductor de Windows Media máscaras,atributo scriptFile en JScript
- atributo skins,scriptFile en JScript
- attributes,scriptFile en JScript
- Atributo scriptFile en JScript
- JScript archivos para máscaras,atributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885313"
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

 

 




