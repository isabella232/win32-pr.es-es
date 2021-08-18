---
description: Un proceso de dos pasos amplía el modelo de Windows del instalador a los productos que contienen ensamblados de Common Language Runtime. Esto permite al instalador revertir instalaciones y eliminaciones de ensamblados incorrectas.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Reversión de ensamblados en la caché global de ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625830"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Reversión de ensamblados en la caché global de ensamblados

Un proceso de dos pasos amplía el modelo de Windows del instalador a los productos que contienen ensamblados de Common Language Runtime. Esto permite al instalador revertir instalaciones y eliminaciones de ensamblados incorrectas.

Durante el primer paso, el instalador de Windows usa microsoft .NET Framework para crear una interfaz para cada ensamblado. El Windows utiliza tantas interfaces como ensamblados estén instalados. Confirmar un ensamblado mediante una de estas interfaces solo significa que el ensamblado está listo para reemplazar cualquier ensamblado existente con el mismo nombre, aún no lo reemplaza. Si el usuario cancela la instalación, o si se produce un error irrespeable de instalación, el instalador de Windows todavía puede revertir el ensamblado a su estado anterior mediante la publicación de estas interfaces.

Una vez que Windows instalador completa la instalación de todos los ensamblados y Windows Installer, el instalador puede iniciar el segundo paso de la instalación. El segundo paso usa una función independiente para realizar la confirmación final de todos los nuevos ensamblados de Common Language Runtime. Esto reemplaza los ensamblados existentes por el mismo nombre.

 

 



