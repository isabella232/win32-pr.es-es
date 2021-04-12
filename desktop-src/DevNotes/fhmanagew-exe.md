---
description: El programa FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino del historial de archivos asignado actualmente.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496186"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

El programa FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino del historial de archivos asignado actualmente.

Este programa está disponible en Windows 8 y Windows Server 2012 y versiones posteriores.

Para ejecutar este programa, vaya al menú **Inicio** , haga clic en **Ejecutar** y escriba el siguiente comando.

*Antigüedad* **de la limpieza deFhManagew.exe**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="age"></span><span id="AGE"></span><em>antig</em><br/></td>
<td>Este parámetro especifica la antigüedad mínima, en días, de las versiones de archivo que se pueden eliminar. Se elimina una versión de archivo si se cumplen las dos condiciones siguientes:<br/>
<ul>
<li>La versión del archivo es anterior a la edad especificada.</li>
<li>El archivo ya no se incluye en el ámbito de protección o hay una versión más reciente del mismo archivo en el dispositivo de destino.</li>
</ul>
Si el parámetro <em>Age</em> está establecido en cero, se eliminarán todas las versiones de archivo, excepto la versión más reciente de cada archivo que se encuentre actualmente en el ámbito de protección.<br/></td>
</tr>
</tbody>
</table>



 

Para suprimir todos los resultados de este programa, use la opción de línea de comandos **-Quiet** como se indica a continuación.

**FhManagew.exe-limpieza** de *edad* **-Quiet**

## <a name="examples"></a>Ejemplos



| Ejemplo                                                                                                                                                                                                      | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-Cleanup 30**<br/>                                 | Elimine todas las versiones de archivo que tengan más de un mes.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-Quiet**<br/> | Elimine todas las versiones de archivo que tengan más de un año y supriman todos los resultados.<br/> |



 

 

 




