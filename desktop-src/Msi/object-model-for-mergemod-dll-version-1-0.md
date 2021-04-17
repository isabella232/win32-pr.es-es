---
description: El modelo de objetos para Mergemod.dll versión 1,0.
ms.assetid: f4180fd6-23a2-4cd9-b309-016f7333e381
title: Modelo de objetos para Mergemod.dll versión 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fb8e1fc923e1fd6433e196ba4ff3f8714ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677539"
---
# <a name="object-model-for-mergemoddll-version-10"></a>Modelo de objetos para Mergemod.dll versión 1,0

El modelo de objetos de Mergemod.dll se organiza de la siguiente manera:

![modelo de objetos para mergemod.dll](images/mergobj.png)

El [objeto Merge](merge-object.md) es el objeto principal del modelo. El [**objeto GetFiles**](getfiles-object.md) es un objeto secundario. Las dependencias son colecciones de [**objetos de dependencia**](dependency-object.md). Los errores son colecciones de [**objetos de error**](error-object.md).

 

 



