---
description: Un proceso de dos pasos extiende el modelo de transacción del Windows Installer a los productos que contienen Common Language Runtime ensamblados. Esto permite que el instalador revierta las instalaciones y eliminaciones de ensamblados que no se hayan realizado correctamente.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversión de ensamblados en la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809488"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Reversión de ensamblados en la caché global de ensamblados

Un proceso de dos pasos extiende el modelo de transacción del Windows Installer a los productos que contienen Common Language Runtime ensamblados. Esto permite que el instalador revierta las instalaciones y eliminaciones de ensamblados que no se hayan realizado correctamente.

En el primer paso, el Windows Installer usa el marco de Microsoft .NET para crear una interfaz para cada ensamblado. En el Windows Installer se usan tantas interfaces como se están instalando los ensamblados. La confirmación de un ensamblado mediante una de estas interfaces solo significa que el ensamblado está listo para reemplazar cualquier ensamblado existente con el mismo nombre, pero aún no lo reemplaza. Si el usuario cancela la instalación o si se produce un error de instalación grave, el Windows Installer puede revertir el ensamblado a su estado anterior mediante la liberación de estas interfaces.

Una vez que la Windows Installer completa la instalación de todos los ensamblados y Windows Installer componentes, el instalador puede iniciar el segundo paso de la instalación. En el segundo paso se usa una función independiente para realizar la confirmación final de todos los nuevos ensamblados de Common Language Runtime. Esto reemplazará todos los ensamblados existentes que tengan el mismo nombre.

 

 



