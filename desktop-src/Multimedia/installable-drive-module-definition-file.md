---
title: Archivo de Module-Definition de unidad instalable
description: Archivo de Module-Definition de unidad instalable
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- Controladores instalables, archivos de definición de módulo
- Controladores instalables, archivos DEF
- Controladores nstallable, función DriverProc
- DriverProc función)
- archivos de definición de módulos
- DEF (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077641"
---
# <a name="installable-drive-module-definition-file"></a>Archivo de Module-Definition de unidad instalable

La definición de módulo (. DEF) de un controlador instalable nombra el controlador, exporta la función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) y define una descripción del controlador. En el ejemplo siguiente se muestra un archivo de definición de módulo típico para un controlador instalable:


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Algunas aplicaciones de instalación pueden abrir el controlador y recuperar la línea de descripción que se va a usar al instalar el controlador. Para seguir siendo compatible con estas aplicaciones de instalación, la línea de descripción debe tener este formato:

  *Alias* \[ de descripción,*alias* \] ... **:* * * texto*

El *alias* especifica un nombre único para el controlador que las aplicaciones pueden usar para abrir el controlador. El alias también sirve como nombre de valor asociado al controlador en el registro. Varios alias se separan mediante comas. El *texto* describe el propósito del controlador.

 

 