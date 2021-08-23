---
description: Agregue un registro a la tabla CustomAction para la acción personalizada Iniciar.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Agregar Launch a las tablas CustomAction y Binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b362259f2ee336a540f396dc05f7745cbc3fde8fb44b8a1c06dabbd6247ba05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145968"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a>Agregar Launch a las tablas CustomAction y Binary

Agregue un registro a la [tabla CustomAction para](customaction-table.md) la acción personalizada Iniciar. Escriba el nombre de la acción personalizada en la columna Acción de la tabla CustomAction. Escriba el tipo numérico total de Inicio, 65, en la columna Tipo de la tabla de acciones Personalizada. La columna Source de la tabla CustomAction especifica una clave en el registro de [la tabla](binary-table.md) binaria que contiene los datos binarios del archivo DLL. Escriba Tutorial.dll en la columna Origen de la tabla CustomAction. El punto de entrada especificado en el campo Destino de la tabla CustomAction debe coincidir con el exportado desde el archivo DLL. Escriba LaunchTutorial en la columna Target de la tabla CustomAction.

[CustomAction (tabla)](customaction-table.md)



| Acción | Tipo | Source       | Destino         |
|--------|------|--------------|----------------|
| Launch | 65   | Tutorial.dll | LaunchTutorial |



 

Agregue la Tutorial.dll que creó a partir de Tutorial.cpp como una secuencia binaria a la tabla Binary.

[Tabla binaria](binary-table.md)



| Nombre         | Datos                          |
|--------------|-------------------------------|
| Tutorial.dll | {*datos binarios agregados para DLL*} |



 

Continúe con [Agregar un evento de control al final de la instalación para ejecutar launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).

 

 



