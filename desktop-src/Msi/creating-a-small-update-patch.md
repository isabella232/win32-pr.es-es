---
description: Siga las instrucciones siguientes al crear una revisión para una actualización pequeña Windows Installer.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Crear una revisión de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158732"
---
# <a name="creating-a-small-update-patch"></a>Crear una revisión de actualización pequeña

Al crear una revisión para [actualizaciones pequeñas,](small-updates.md)los autores deben cumplir las siguientes directrices:

-   Las revisiones de actualización pequeñas deben diseñarse para una instalación de destino única.
-   Las revisiones de actualización pequeñas deben usar la versión más antigua como instalación de destino.
-   Una revisión de actualización pequeña debe reemplazar y dejar obsoletas las revisiones de actualización pequeñas anteriores.

En el siguiente escenario se muestra cuándo es mejor una revisión de actualización pequeña.

Su empresa envía la versión 1.0 de Myproduct.msi. Poco después, se envía una pequeña [revisión de](small-updates.md) actualización para Myproduct.msi llamada QFE1. Esto no cambia la [**propiedad ProductCode**](productcode.md) ni [**la propiedad ProductVersion.**](productversion.md)

Más adelante, cree una segunda [revisión de actualización](small-updates.md) pequeña para Myproduct.msi llamada QFE2. Esta segunda revisión debe tener como Myproduct.msi versión 1.0. Esta segunda revisión no debe tener como destino Myproduct.msi versión 1.0 y Myproduct.msi versión 1.0 + QFE1. Cuando se aplica QFE2, debe quitar QFE1.

 

 



