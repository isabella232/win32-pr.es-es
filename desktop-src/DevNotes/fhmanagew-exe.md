---
description: El FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino Historial de archivos asignado actualmente.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcf8480117dd9d10bf001682bd2c789290e2cebb0369d72afe9624ea1aefd48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538745"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

El FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino Historial de archivos asignado actualmente.

Este programa está disponible en Windows 8 y Windows Server 2012 y versiones posteriores.

Para ejecutar este programa, vaya al **menú** Inicio, haga clic **en Ejecutar** y escriba el siguiente comando.

**FhManagew.exe -cleanup** *age*



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
<td><span id="age"></span><span id="AGE"></span><em>Edad</em><br/></td>
<td>Este parámetro especifica la antigüedad mínima, en días, de las versiones de archivo que se pueden eliminar. Se elimina una versión de archivo si se cumplen las dos condiciones siguientes:<br/>
<ul>
<li>La versión del archivo es anterior a la edad especificada.</li>
<li>El archivo ya no se incluye en el ámbito de protección o hay una versión más reciente del mismo archivo en el dispositivo de destino.</li>
</ul>
Si el <em>parámetro age</em> se establece en cero, se eliminan todas las versiones de archivo, excepto la versión más reciente de cada archivo que está presente actualmente en el ámbito de protección.<br/></td>
</tr>
</tbody>
</table>



 

Para suprimir todos los resultados de este programa, use la opción de línea de comandos **-quiet** como se muestra a continuación.

**FhManagew.exe -cleanup** *age* **-quiet**

## <a name="examples"></a>Ejemplos



| Ejemplo                                                                                                                                                                                                      | Descripción                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**<br/>                                 | Elimine todas las versiones de archivo anteriores a un mes.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**<br/> | Elimine todas las versiones de archivo anteriores a un año y suprima todas las salidas.<br/> |



 

 

 




