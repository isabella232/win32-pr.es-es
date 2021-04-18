---
description: Incluye el contenido de un archivo MOF en otro archivo MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697646"
---
# <a name="include"></a>' #include '
/* Title: MyMof. mof                           *//*   title: MyMof2. mof */

El \# comando incluir preprocesador incluye el contenido de un archivo MOF en otro archivo MOF. En el ejemplo de código siguiente se describe la sintaxis del \# comando include.

``` syntax
#include ("Moffile.mof")
```

En el ejemplo anterior, Moffile. mof es el nombre del archivo MOF que se va a incluir.

En el ejemplo siguiente se muestran dos archivos MOF. Al compilar el primer archivo MOF, el compilador compila automáticamente el segundo archivo MOF (Mymof2. mof) en la ubicación donde se coloca la \# instrucción include.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

El siguiente archivo MOF se incluye en el ejemplo anterior:

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



