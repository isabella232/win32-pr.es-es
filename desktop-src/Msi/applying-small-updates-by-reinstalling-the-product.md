---
description: Una actualización pequeña se puede aplicar a una aplicación mediante la reinstalación completa o parcial de la aplicación desde la línea de comandos o desde un programa.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Aplicar actualizaciones pequeñas reinstalando el producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001746"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a><span data-ttu-id="132da-103">Aplicar actualizaciones pequeñas reinstalando el producto</span><span class="sxs-lookup"><span data-stu-id="132da-103">Applying Small Updates by Reinstalling the Product</span></span>

<span data-ttu-id="132da-104">Una actualización pequeña se puede aplicar a una aplicación mediante la reinstalación completa o parcial de la aplicación desde la línea de comandos o desde un programa.</span><span class="sxs-lookup"><span data-stu-id="132da-104">A small update can be applied to an application by completely or partially reinstalling the application from the command line or from a program.</span></span>

<span data-ttu-id="132da-105">**Para propagar la actualización pequeña a los usuarios actuales (se trata de una reinstalación completa) desde la línea de comandos**</span><span class="sxs-lookup"><span data-stu-id="132da-105">**To propagate the small update to current users (this is a complete reinstall) from the command line**</span></span>

1.  <span data-ttu-id="132da-106">Desde la línea de comandos, use: **msiexec \[ /fvomus** _ruta de acceso para actualizar el archivo. msi_ *_\]_* o **msiexec/i \[** _path para actualizar el archivo. msi_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.</span><span class="sxs-lookup"><span data-stu-id="132da-106">From the command line use either: **msiexec /fvomus \[**_path to updated .msi file_*_\]_* or **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=ALL REINSTALLMODE=vomus_*.</span></span>
2.  <span data-ttu-id="132da-107">El archivo. msi actualizado se almacena en caché en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="132da-107">The updated .msi file is cached on the user's computer.</span></span> <span data-ttu-id="132da-108">Tenga en cuenta que no es posible que el usuario vuelva a instalar el producto mediante agregar o quitar programas, ya que el archivo. msi actualizado aún no se encuentra en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="132da-108">Note that it is not possible for the user to reinstall the product using Add/Remove Programs because the updated .msi file is not yet on the user's computer.</span></span>

<span data-ttu-id="132da-109">**Para propagar una pequeña actualización a los usuarios actuales (se trata de una reinstalación completa) de un programa**</span><span class="sxs-lookup"><span data-stu-id="132da-109">**To propagate a small update to current users (this is a complete reinstall) from a program**</span></span>

1.  <span data-ttu-id="132da-110">En un programa, llame a [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) y especifique el \_ método REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ USERDATA y REINSTALLMODE \_ .</span><span class="sxs-lookup"><span data-stu-id="132da-110">From a program, call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) and specify REINSTALLMODE\_PACKAGE, REINSTALLMODE\_FILEOLDERVERSION, REINSTALLMODE\_MACHINEDATA, REINSTALLMODE\_USERDATA, and REINSTALLMODE\_SHORTCUT</span></span>
2.  <span data-ttu-id="132da-111">El archivo. msi actualizado se almacena en caché en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="132da-111">The updated .msi file is cached on the user's computer.</span></span>

<span data-ttu-id="132da-112">El método siguiente inicia una reinstalación de solo las características o los componentes que se ven afectados por la actualización pequeña.</span><span class="sxs-lookup"><span data-stu-id="132da-112">The following method launches a reinstallation of only those features or components that are affected by the small update.</span></span>

<span data-ttu-id="132da-113">**Para propagar una pequeña actualización a los usuarios actuales (se trata de una reinstalación parcial)**</span><span class="sxs-lookup"><span data-stu-id="132da-113">**To propagate a small update to current users (this is a partial reinstall)**</span></span>

1.  <span data-ttu-id="132da-114">Obtenga una lista de los nombres de las características y los componentes que se ven afectados por la actualización pequeña.</span><span class="sxs-lookup"><span data-stu-id="132da-114">Obtain a list of the names of features and components that are affected by the small update.</span></span>
2.  <span data-ttu-id="132da-115">En el símbolo del sistema, use **: \[ msiexec/i** _rutaDeAcceso para actualizar el archivo. msi_ *_\] REINSTALL = \[_* lista _\] de características_ **REINSTALLMODE = vomus**.</span><span class="sxs-lookup"><span data-stu-id="132da-115">From the command prompt use: **msiexec /I \[**_path to updated .msi file_*_\] REINSTALL=\[_*_Feature list\]_ **REINSTALLMODE=vomus**.</span></span>
3.  <span data-ttu-id="132da-116">El archivo. msi actualizado se almacena en caché en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="132da-116">The updated .msi file is cached on the user's computer.</span></span>

 

 



