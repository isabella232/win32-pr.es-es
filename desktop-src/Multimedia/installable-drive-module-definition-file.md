---
title: Archivo de Module-Definition unidad instalable
description: Archivo de Module-Definition unidad instalable
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- controladores instalables, archivos de definición de módulo
- controladores instalables, archivos DEF
- nstallable drivers,DriverProc (Función)
- Función DriverProc
- archivos de definición de módulo
- DEF (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372278"
---
# <a name="installable-drive-module-definition-file"></a>Archivo de Module-Definition unidad instalable

La definición del módulo (. DEF) de un controlador instalable denomina al controlador, exporta la [función DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) y define una descripción del controlador. En el ejemplo siguiente se muestra un archivo de definición de módulo típico para un controlador instalable:


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Algunas aplicaciones de instalación pueden abrir el controlador y recuperar la línea de descripción que se usará al instalar el controlador. Para seguir siendo compatible con estas aplicaciones de instalación, la línea de descripción debe tener este formato:

**Alias DESCRIPTION,** \[ *alias* \] ... **:**_texto_  

El *alias* especifica un nombre único para el controlador que las aplicaciones pueden usar para abrir el controlador. El alias también actúa como el nombre de valor asociado al controlador en el Registro. Varios alias están separados por comas. El *texto* describe el propósito del controlador.

 

 