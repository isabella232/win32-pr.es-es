---
description: Una instalación administrativa crea una imagen de origen de una aplicación o un producto en una red.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02c8e3eb606dc92c60a86dd8e3216cbc99603200a87e5ee5dda0983fb7ad34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559165"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa

Una [instalación administrativa](administrative-installation.md) crea una imagen de origen de una aplicación o un producto en una red. Los usuarios de un grupo de trabajo que tienen acceso a esta imagen administrativa pueden instalar el producto desde este origen. La actualización de la aplicación para este grupo de trabajo se realiza en dos pasos:

-   En primer lugar, la revisión de actualización pequeña se puede aplicar a la imagen administrativa.
-   En segundo lugar, los cambios en la actualización pequeña deben propagarse a los usuarios.

**Para aplicar una pequeña revisión de actualización a una imagen administrativa**

1.  Obtenga la pequeña actualización en forma de un paquete [de revisión](patch-packages.md). Por ejemplo, la pequeña actualización denominada Patch.msp.
2.  Obtenga la ruta de acceso a la imagen administrativa.
3.  Desde la línea de comandos, use:

    **msiexec /a** *\[ path to administrative image \] .msi file* **/p** *patch.msp*

4.  Esto actualiza los archivos de aplicación y el .msi de la imagen administrativa. Para obtener una lista de las opciones que se pueden usar con Msiexec.exe, vea [Opciones de línea de comandos](command-line-options.md). Windows El instalador determina automáticamente si la imagen administrativa usa nombres de archivo cortos y establece la [**propiedad SHORTFILENAMES.**](shortfilenames.md)
5.  La imagen administrativa resultante es la misma que la que genera una instalación administrativa mediante un CD-ROM de producto completo que incluye la actualización. Cuando los nuevos usuarios instalan la aplicación desde este origen, reciben la aplicación actualizada.

**Para propagar la pequeña actualización al grupo de trabajo**

-   Los miembros del grupo de trabajo obtienen los cambios reinstalando la aplicación desde la imagen administrativa mediante el procedimiento descrito en Aplicar pequeñas actualizaciones [reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md).

 

 



