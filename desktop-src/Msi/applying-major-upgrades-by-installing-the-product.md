---
description: Se puede aplicar una actualización principal instalando el nuevo paquete de instalación para el producto actualizado.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Aplicación de actualizaciones principales mediante la instalación del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159125"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Aplicación de actualizaciones principales mediante la instalación del producto

Se puede aplicar una actualización principal instalando el nuevo paquete de instalación para el producto actualizado. Dado que las actualizaciones principales obtienen un código de producto diferente al producto original, la instalación de la actualización debe tratarse como una instalación de un nuevo producto. La actualización simplemente se puede instalar como otro producto. Puede hacer que el nuevo paquete de instalación controle la eliminación del producto anterior incluyendo la tabla Actualizar y la acción [FindRelatedProducts](findrelatedproducts-action.md) y [la acción RemoveExistingProducts](removeexistingproducts-action.md). [](upgrade-table.md)

**Para propagar una actualización principal a los usuarios actuales desde la línea de comandos**

-   Desde la línea de comandos, use: **msiexec /i \[** _path to updated msi file_*_\]_*

**Para propagar una actualización principal a los usuarios actuales desde un programa**

-   Desde un programa, llame [**a MsiInstallProduct y**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) especifique la ruta de acceso al archivo msi actualizado.

 

 



