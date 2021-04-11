---
description: Para instalar un archivo, una fuente o una clave del registro para que no se quite cuando se desinstale el producto, el componente completo que contiene el archivo, la fuente o la clave del registro debe ser permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalación de componentes permanentes, archivos, fuentes y claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083444"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a><span data-ttu-id="bfde6-103">Instalación de componentes permanentes, archivos, fuentes y claves del registro</span><span class="sxs-lookup"><span data-stu-id="bfde6-103">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>

<span data-ttu-id="bfde6-104">Para instalar un archivo, una fuente o una clave del registro para que no se quite cuando se desinstale el producto, el componente completo que contiene el archivo, la fuente o la clave del registro debe ser permanente.</span><span class="sxs-lookup"><span data-stu-id="bfde6-104">To install a file, font, or registry key so that it is not removed when the product is uninstalled, the entire component containing the file, font, or registry key must be made permanent.</span></span> <span data-ttu-id="bfde6-105">Para que un componente sea permanente, establezca **msidbComponentAttributesPermanent** en la columna Attributes de la [tabla Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="bfde6-105">To make a component permanent, set **msidbComponentAttributesPermanent** in the Attributes column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="bfde6-106">Tenga en cuenta que el instalador quita una clave del registro después de quitar el último valor o subclave de la clave.</span><span class="sxs-lookup"><span data-stu-id="bfde6-106">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="bfde6-107">Para evitar que se quite una clave del Registro vacía al desinstalar, escriba un valor ficticio en la clave que necesita conservar y escriba + en la columna Nombre de la [tabla del registro](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="bfde6-107">To prevent an empty registry key from being removed on uninstall, write a dummy value under the key you need keep, and enter + in the Name column of the [Registry table](registry-table.md).</span></span>

 

 



