---
description: Es similar a un modificador de línea de comandos. Sin embargo, no es necesario volver a escribir un \# comando pragma cada vez que compile un archivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3cb9541ceef51119ce521244282920ca88397afe13290e99bdc14ce7d98ab55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860565"
---
# <a name="pragma"></a>\#Pragma

El **\# comando de preprocesador pragma** es similar a un modificador de línea de comandos. Sin embargo, no es necesario volver a escribir un **\# comando pragma** cada vez que compile un archivo MOF. En el ejemplo siguiente se muestra la **\# sintaxis de comandos pragma:**


```mof
#pragma [command]
```



Normalmente, se coloca **\# un comando pragma** al principio de un archivo MOF. Sin embargo, puede colocar algunos comandos, como el **\# comando pragma,** en el cuerpo del código MOF. En el ejemplo siguiente se muestran comandos **\# pragma** que indican al compilador MOF que debe colocar clases e instancias en el espacio de nombres cimv2 raíz y compilar el archivo en el que se incluyen los comandos durante la recuperación del \\ repositorio:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



A continuación se enumeran los **\# comandos pragma** disponibles.



| Get-Help                                         | Descripción                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Enmienda**](pragma-amendment.md)           | Dirige al compilador MOF para separar un archivo MOF en versiones independientes del lenguaje y específicas del lenguaje. |
| [**Autorrecuperación**](pragma-autorecover.md)       | Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.                             |
| [**classflags**](pragma-classflags.md)         | Controla la forma en que se crean o actualizan las clases en función de las marcas especificadas.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Elimina una clase existente y sus instancias del repositorio.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Elimina una instancia existente de una clase del repositorio.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.                   |
| [**Nombres**](pragma-namespace.md)           | Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*.         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



