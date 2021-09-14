---
description: Puede aplicar la pequeña actualización a una instalación local de MNP2000 con la revisión de ejemplo MNTchtch.msp creada en Generar un paquete de revisión.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicar un paquete de revisión a una instalación local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159129"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Aplicar un paquete de revisión a una instalación local

Puede aplicar la pequeña actualización a una instalación local de MNP2000 con la revisión de ejemplo MNTchtch.msp creada en [Generar un paquete de revisión](generating-a-patch-package.md). El procedimiento general se describe en la sección [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Instale el producto MNP2000 original localmente en el equipo. Compruebe que esto tiene el error Concert.txt que la actualización pequeña se va a corregir. A continuación, escriba la siguiente línea de comandos para iniciar la instalación.

**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**

Vuelva a examinar el Concert.txt que pertenece a MNP2000 para comprobar que el instalador ha aplicado la pequeña actualización para corregir este archivo.

Para aplicar la pequeña actualización a una imagen administrativa, vea [Aplicar un paquete de revisión a una instalación administrativa.](applying-a-patch-package-to-an-administrative-installation.md)

[Continuar](applying-a-patch-package-to-an-administrative-installation.md)

 

 



