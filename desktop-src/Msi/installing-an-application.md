---
description: Puede instalar productos completos con funciones de Windows Installer. En los pasos siguientes se describe cómo instalar un producto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Instalación de una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668409"
---
# <a name="installing-an-application"></a><span data-ttu-id="9ea14-104">Instalación de una aplicación</span><span class="sxs-lookup"><span data-stu-id="9ea14-104">Installing an Application</span></span>

<span data-ttu-id="9ea14-105">Puede instalar productos completos con funciones de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9ea14-105">You can install entire products with Windows Installer functions.</span></span> <span data-ttu-id="9ea14-106">En los pasos siguientes se describe cómo instalar un producto.</span><span class="sxs-lookup"><span data-stu-id="9ea14-106">The following steps describe how to install a product.</span></span>

<span data-ttu-id="9ea14-107">**Para instalar un producto**</span><span class="sxs-lookup"><span data-stu-id="9ea14-107">**To install a product**</span></span>

1.  <span data-ttu-id="9ea14-108">Ejecute un producto a través de su secuencia de instalación o desinstalación mediante una llamada a la función [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .</span><span class="sxs-lookup"><span data-stu-id="9ea14-108">Run a product through its installation or uninstallation sequence by calling the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function.</span></span>
2.  <span data-ttu-id="9ea14-109">Especifique el nivel de instalación mediante una llamada a la función [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .</span><span class="sxs-lookup"><span data-stu-id="9ea14-109">Specify the installation level by calling the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function.</span></span>

    <span data-ttu-id="9ea14-110">Puede usar los parámetros de la función [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) para establecer el estado de la instalación.</span><span class="sxs-lookup"><span data-stu-id="9ea14-110">You can use the parameters of the [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) function to set the installation state.</span></span> <span data-ttu-id="9ea14-111">Por ejemplo, puede establecer el estado para instalar localmente o para instalar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="9ea14-111">For example, you can set the state to install locally or to install from the source.</span></span> <span data-ttu-id="9ea14-112">Puede establecer el intervalo de características del producto que se van a incluir estableciendo el nivel.</span><span class="sxs-lookup"><span data-stu-id="9ea14-112">You can set the range of product features to be included by setting the level.</span></span>

<span data-ttu-id="9ea14-113">Para obtener más información sobre la instalación de una aplicación, consulte el [mecanismo de instalación](installation-mechanism.md)y [resistencia](resiliency.md) .</span><span class="sxs-lookup"><span data-stu-id="9ea14-113">For more information about installing an application, see [Resiliency](resiliency.md) and [Installation Mechanism](installation-mechanism.md).</span></span>

 

 



