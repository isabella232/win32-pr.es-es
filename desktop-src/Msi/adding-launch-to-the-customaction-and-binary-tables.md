---
description: Agregue un registro a la tabla CustomAction para la acción personalizada Launch.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Adición del inicio a las tablas de CustomAction y binarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156352"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Adición del inicio a las tablas de CustomAction y binarias

Agregue un registro a la [tabla CustomAction](customaction-table.md) para la acción personalizada Launch. Escriba el nombre de la acción personalizada en la columna Acción de la tabla CustomAction. Escriba el tipo numérico total para el inicio, 65, en la columna tipo de la tabla de acciones personalizadas. La columna de origen de la tabla CustomAction especifica una clave en el registro de la [tabla binaria](binary-table.md) que contiene los datos binarios de la dll. Escriba Tutorial.dll en la columna origen de la tabla CustomAction. El punto de entrada especificado en el campo de destino de la tabla CustomAction debe coincidir con el exportado desde el archivo DLL. Escriba LaunchTutorial en la columna target de la tabla CustomAction.

[Tabla CustomAction](customaction-table.md)



| Acción | Tipo | Source       | Destino         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | LaunchTutorial |



 

Agregue el Tutorial.dll que creó en tutorial. cpp como una secuencia binaria a la tabla binaria.

[Tabla binaria](binary-table.md)



| Nombre         | Datos                          |
|--------------|-------------------------------|
| Tutorial.dll | {*datos binarios agregados para dll*} |



 

Continúe [agregando un evento de control al final de la instalación para ejecutar el inicio](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



