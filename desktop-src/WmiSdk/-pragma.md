---
description: Es similar a un modificador de la línea de comandos. Sin embargo, no es necesario volver a escribir un \# comando pragma cada vez que se compila un archivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697647"
---
# <a name="pragma"></a>\#pragma

El comando de preprocesador **\# pragma** es similar a un modificador de la línea de comandos. Sin embargo, no es necesario volver a escribir un comando **\# pragma** cada vez que se COMPILA un archivo MOF. En el ejemplo siguiente se muestra la sintaxis del comando **\# pragma** :


```mof
#pragma [command]
```



Normalmente, se coloca un comando **\# pragma** al principio de un archivo MOF. No obstante, puede colocar algunos comandos, como el comando **\# pragma** , en el cuerpo del código MOF. En el ejemplo siguiente se muestran comandos **\# pragma** que indican al compilador MOF que debe colocar clases e instancias en el \\ espacio de nombres root cimv2 y compilar el archivo en el que se incluyen los comandos durante la recuperación del repositorio:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



A continuación se enumeran los comandos de **\# pragma** disponibles.



| Get-Help                                         | Descripción                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**corrección**](pragma-amendment.md)           | Indica al compilador MOF que separe un archivo MOF en versiones independientes del lenguaje y específicas del idioma. |
| [**Autorrecuperación**](pragma-autorecover.md)       | Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.                             |
| [**classflags**](pragma-classflags.md)         | Controla la forma en que se crean o actualizan las clases según las marcas especificadas.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Elimina una clase existente y sus instancias del repositorio.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Elimina una instancia existente de una clase del repositorio.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.                   |
| [**namespace**](pragma-namespace.md)           | Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*.         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



