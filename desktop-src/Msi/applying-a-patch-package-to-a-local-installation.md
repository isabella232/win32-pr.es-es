---
description: Puede aplicar la actualización pequeña a una instalación local de MNP2000 con la revisión de ejemplo MNPpatch. MSP creada en la generación de un paquete de revisión.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicar un paquete de revisión a una instalación local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276527"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Aplicar un paquete de revisión a una instalación local

Puede aplicar la actualización pequeña a una instalación local de MNP2000 con la revisión de ejemplo MNPpatch. MSP creada en la [generación de un paquete de revisión](generating-a-patch-package.md). El procedimiento general se describe en la sección [aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Instale el producto MNP2000 original localmente en el equipo. Compruebe que tiene el error Concert.txt que la actualización pequeña se va a corregir. Después, inicie la instalación escribiendo la siguiente línea de comandos.

**msiexec/p MNP2000. MSP REINSTALL = ALL REINSTALLMODE = OMUs**

Reexamine el Concert.txt que pertenece a MNP2000 para comprobar que el instalador ha aplicado la actualización pequeña para corregir este archivo.

Para aplicar la actualización pequeña a una imagen administrativa, consulte [aplicar un paquete de revisión a una instalación administrativa](applying-a-patch-package-to-an-administrative-installation.md).

[Continuar](applying-a-patch-package-to-an-administrative-installation.md)

 

 



