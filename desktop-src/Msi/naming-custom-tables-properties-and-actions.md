---
description: Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de las tablas, propiedades o acciones estándar que son nativas para el Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Asignar nombres a tablas, propiedades y acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908707"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Asignar nombres a tablas, propiedades y acciones personalizadas

Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de las tablas, propiedades o acciones estándar que son nativas para el Windows Installer.

Los autores de paquetes deben cumplir las siguientes directrices para los nombres de tabla, propiedad o acción personalizados.

-   Cree nombres para las tablas, las propiedades o las acciones personalizadas que tengan un prefijo que identifique la aplicación.
-   Nunca use un nombre con MSI como prefijo. A partir de Windows Installer 2,0, todas las nuevas propiedades, acciones y tablas de Windows Installer nativas reciben nombres con el prefijo MSI. Este prefijo no distingue entre mayúsculas y minúsculas, por ejemplo MsiNewInternalTable. Dado que el prefijo no distingue entre mayúsculas y minúsculas, los autores deben evitar todos los casos del prefijo MSI.

Para obtener más información, vea [nombres de tabla](table-names.md).

 

 



