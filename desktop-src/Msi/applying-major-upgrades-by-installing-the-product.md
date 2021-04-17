---
description: Se puede aplicar una actualización principal mediante la instalación del nuevo paquete de instalación para el producto actualizado.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Aplicar las actualizaciones principales instalando el producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652615"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Aplicar las actualizaciones principales instalando el producto

Se puede aplicar una actualización principal mediante la instalación del nuevo paquete de instalación para el producto actualizado. Dado que las actualizaciones principales obtienen un código de producto diferente del producto original, la instalación de la actualización debe tratarse como una instalación de un nuevo producto. La actualización se puede instalar simplemente como otro producto. Puede hacer que el nuevo paquete de instalación controle la eliminación del producto anterior incluyendo la [tabla de actualización](upgrade-table.md) y la acción [FindRelatedProducts](findrelatedproducts-action.md) y la [acción RemoveExistingProducts](removeexistingproducts-action.md).

**Para propagar una actualización principal a los usuarios actuales desde la línea de comandos**

-   Desde la línea de comandos, use: **msiexec \[ /i** _path to Updated MSI File_ .*_\]_*

**Para propagar una actualización principal a los usuarios actuales desde un programa**

-   En un programa, llame a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) y especifique la ruta de acceso al archivo MSI actualizado.

 

 



