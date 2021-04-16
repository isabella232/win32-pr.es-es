---
title: Llamadas a funciones
description: Llamadas a funciones
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Aspectos de Windows Media Player, llamar a funciones en JScript
- máscaras, llamar a funciones en JScript
- llamar a funciones en JScript
- Archivos JScript para máscaras, llamar a funciones
- Aspectos de Windows Media Player, atributo scriptFile en JScript
- máscaras, atributo scriptFile en JScript
- atributos, scriptFile en JScript
- atributo scriptFile en JScript
- Archivos JScript para máscaras, atributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532463"
---
# <a name="calling-functions"></a>Llamadas a funciones

Si necesita llamar a más de unas pocas líneas de código, puede cargar un archivo de script mediante el atributo **scriptFile** del elemento **View** y llamar a las funciones del script. Puede cargar más de un archivo por vista:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Una vez cargados los archivos de script, puede llamar a funciones de dentro de la sección de vista. Por ejemplo, para llamar a *una función llamada myFunction cuando se* haga clic en algo, escriba lo siguiente:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Si tiene más de una vista, solo las funciones de los archivos cargados en la vista actual estarán disponibles para el código XML y JScript que se ejecuta con la vista actual. Los archivos cargados en otras vistas no están en el ámbito de la vista actual.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar JScript**](using-jscript.md)
</dt> </dl>

 

 




