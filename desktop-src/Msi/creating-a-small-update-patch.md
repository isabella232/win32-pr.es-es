---
description: Siga las instrucciones que se indican a continuación al crear una revisión para una Windows Installer actualización pequeña.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Crear una revisión de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669750"
---
# <a name="creating-a-small-update-patch"></a>Crear una revisión de actualización pequeña

Al crear una revisión para [las actualizaciones pequeñas](small-updates.md), los autores deben cumplir las siguientes directrices:

-   Las revisiones de actualización pequeñas deben diseñarse para una única instalación de destino.
-   Las revisiones de actualización pequeñas deben usar la versión más antigua como la instalación de destino.
-   Una revisión de actualización pequeña debe reemplazar y hacer que las revisiones de actualización pequeñas anteriores queden obsoletas.

El siguiente escenario muestra Cuándo es mejor una pequeña revisión de actualización.

Su empresa incluye la versión 1,0 de Myproduct.msi. Poco después, envía una pequeña revisión de [actualización](small-updates.md) para Myproduct.msi denominada QFE1. Esto no cambia la propiedad [**ProductCode**](productcode.md) o la propiedad [**ProductVersion**](productversion.md) .

Más adelante, creará una segunda revisión de [actualización pequeña](small-updates.md) para Myproduct.msi denominada QFE2. Esta segunda revisión debe tener como destino Myproduct.msi versión 1,0. Esta segunda revisión no debe tener como destino Myproduct.msi versión 1,0 y Myproduct.msi versión 1,0 + QFE1. Cuando se aplica QFE2, debe quitar QFE1.

 

 



