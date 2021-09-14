---
description: Agregue un registro a la tabla CustomAction para la acción iniciar personalizada.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Agregar Launch a las tablas CustomAction y Binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159208"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Agregar Launch a las tablas CustomAction y Binary

Agregue un registro a la [tabla CustomAction para](customaction-table.md) la acción iniciar personalizada. Escriba el nombre de la acción personalizada en la columna Acción de la tabla CustomAction. Escriba el tipo numérico total de Launch, 65, en la columna Tipo de la tabla de acciones personalizadas. La columna Source de la tabla CustomAction especifica una clave en el registro de [la tabla](binary-table.md) binaria que contiene los datos binarios del archivo DLL. Escriba Tutorial.dll en la columna Origen de la tabla CustomAction. El punto de entrada especificado en el campo Destino de la tabla CustomAction debe coincidir con el exportado desde el archivo DLL. Escriba LaunchTutorial en la columna Destino de la tabla CustomAction.

[Tabla CustomAction](customaction-table.md)



| Acción | Tipo | Source       | Destino         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | LaunchTutorial |



 

Agregue el Tutorial.dll que creó desde Tutorial.cpp como un flujo binario a la tabla Binary.

[Tabla binaria](binary-table.md)



| Nombre         | Datos                          |
|--------------|-------------------------------|
| Tutorial.dll | {*datos binarios agregados para DLL*} |



 

Continúe con [Agregar un evento de control al final de la instalación para ejecutar launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



