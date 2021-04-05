---
description: Una instalación administrativa crea una imagen de origen de una aplicación o un producto en una red.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001748"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa

Una [instalación administrativa](administrative-installation.md) crea una imagen de origen de una aplicación o un producto en una red. Los usuarios de un grupo de trabajo que tengan acceso a esta imagen administrativa pueden instalar el producto desde este origen. La actualización de la aplicación para este grupo de trabajo se realiza en dos pasos:

-   En primer lugar, se puede aplicar la revisión de actualización pequeña a la imagen administrativa.
-   En segundo lugar, los cambios en la actualización pequeña deben propagarse a los usuarios.

**Para aplicar una pequeña revisión de actualización a una imagen administrativa**

1.  Obtenga la actualización pequeña en forma de paquete de [revisión](patch-packages.md). Por ejemplo, la actualización pequeña denominada patch. msp.
2.  Obtenga la ruta de acceso a la imagen administrativa.
3.  En la línea de comandos, use:

    **msiexec/a** *\[ ruta de acceso al archivo \] . msi de la imagen administrativa* **/p** *patch. MSP*

4.  De esta forma se actualizan los archivos de aplicación y el archivo. msi de la imagen administrativa. Para obtener una lista de las opciones que se pueden utilizar con Msiexec.exe, vea opciones de la [línea de comandos](command-line-options.md). Windows Installer determina automáticamente si la imagen administrativa usa nombres de archivo cortos y establece la propiedad [**SHORTFILENAMES**](shortfilenames.md) .
5.  La imagen administrativa resultante es la misma que la generada por una instalación administrativa con un CD-ROM completo del producto que incluye la actualización. Cuando los nuevos usuarios instalan la aplicación desde este origen, reciben la aplicación actualizada.

**Para propagar la pequeña actualización al grupo de trabajo**

-   Los miembros del grupo de trabajo obtienen los cambios reinstalando la aplicación a partir de la imagen administrativa mediante el procedimiento descrito en [aplicación de actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md).

 

 



