---
description: El FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino Historial de archivos asignado actualmente.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2570da9b2b874b723b28917028fab3c58ecdf772
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481521"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

El FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino Historial de archivos asignado actualmente.

Este programa está disponible en Windows 8 y Windows Server 2012 y versiones posteriores.

Para ejecutar este programa, vaya al **menú** Inicio, haga clic **en Ejecutar** y escriba el siguiente comando.

**FhManagew.exe -cleanup** *age*




| Parámetro | Descripción | 
|-----------|-------------|
| <span id="age"></span><span id="AGE"></span><em>Edad</em><br /> | Este parámetro especifica la antigüedad mínima, en días, de las versiones de archivo que se pueden eliminar. Se elimina una versión de archivo si se cumplen las dos condiciones siguientes:<br /><ul><li>La versión del archivo es anterior a la edad especificada.</li><li>El archivo ya no se incluye en el ámbito de protección o hay una versión más reciente del mismo archivo en el dispositivo de destino.</li></ul>Si el <em>parámetro age</em> se establece en cero, se eliminan todas las versiones de archivo, excepto la versión más reciente de cada archivo que está presente actualmente en el ámbito de protección.<br /> | 




 

Para suprimir todas las salidas de este programa, use la opción de línea de comandos **-quiet** como se muestra a continuación.

**FhManagew.exe -cleanup** *age* **-quiet**

## <a name="examples"></a>Ejemplos



| Ejemplo                                                                                                                                                                                                      | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**<br/>                                 | Elimine todas las versiones de archivo anteriores a un mes.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**<br/> | Elimine todas las versiones de archivo anteriores a un año y suprima todas las salidas.<br/> |



 

 

 




