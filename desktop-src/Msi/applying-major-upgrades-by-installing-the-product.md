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
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="25c84-103">Aplicar las actualizaciones principales instalando el producto</span><span class="sxs-lookup"><span data-stu-id="25c84-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="25c84-104">Se puede aplicar una actualización principal mediante la instalación del nuevo paquete de instalación para el producto actualizado.</span><span class="sxs-lookup"><span data-stu-id="25c84-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="25c84-105">Dado que las actualizaciones principales obtienen un código de producto diferente del producto original, la instalación de la actualización debe tratarse como una instalación de un nuevo producto.</span><span class="sxs-lookup"><span data-stu-id="25c84-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="25c84-106">La actualización se puede instalar simplemente como otro producto.</span><span class="sxs-lookup"><span data-stu-id="25c84-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="25c84-107">Puede hacer que el nuevo paquete de instalación controle la eliminación del producto anterior incluyendo la [tabla de actualización](upgrade-table.md) y la acción [FindRelatedProducts](findrelatedproducts-action.md) y la [acción RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="25c84-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="25c84-108">**Para propagar una actualización principal a los usuarios actuales desde la línea de comandos**</span><span class="sxs-lookup"><span data-stu-id="25c84-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="25c84-109">Desde la línea de comandos, use: **msiexec \[ /i** _path to Updated MSI File_ .*_\]_*</span><span class="sxs-lookup"><span data-stu-id="25c84-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="25c84-110">**Para propagar una actualización principal a los usuarios actuales desde un programa**</span><span class="sxs-lookup"><span data-stu-id="25c84-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="25c84-111">En un programa, llame a [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) y especifique la ruta de acceso al archivo MSI actualizado.</span><span class="sxs-lookup"><span data-stu-id="25c84-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



