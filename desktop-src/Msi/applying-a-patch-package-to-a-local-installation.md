---
description: Puede aplicar la pequeña actualización a una instalación local de MNP2000 con la revisión de ejemplo MNTchtch.msp creada en Generación de un paquete de revisión.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicar un paquete de revisión a una instalación local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db0f29c5ced78ff8f5ad4ce8c667ba7265dd7426f9a34a5d17f743e07bfc6ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078125"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Aplicar un paquete de revisión a una instalación local

Puede aplicar la pequeña actualización a una instalación local de MNP2000 con la revisión de ejemplo MNTchtch.msp creada en [Generación de un paquete de revisión](generating-a-patch-package.md). El procedimiento general se describe en la sección Aplicar pequeñas actualizaciones mediante la aplicación de revisiones [a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Instale el producto MNP2000 original localmente en el equipo. Compruebe que tiene el error Concert.txt que se va a corregir la actualización pequeña. A continuación, inicie la instalación especificando la siguiente línea de comandos.

**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**

Vuelva a examinar el Concert.txt que pertenece a MNP2000 para comprobar que el instalador ha aplicado la pequeña actualización para corregir este archivo.

Para aplicar la pequeña actualización a una imagen administrativa, consulte [Aplicar un paquete de revisión a una instalación administrativa.](applying-a-patch-package-to-an-administrative-installation.md)

[Continuar](applying-a-patch-package-to-an-administrative-installation.md)

 

 



