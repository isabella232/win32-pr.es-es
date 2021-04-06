---
description: El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK de Windows Installer como archivo tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Crear la acción personalizada iniciar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001721"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="b855a-103">Crear la acción personalizada iniciar</span><span class="sxs-lookup"><span data-stu-id="b855a-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="b855a-104">El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK de Windows Installer como archivo tutorial. cpp.</span><span class="sxs-lookup"><span data-stu-id="b855a-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="b855a-105">Esta acción personalizada usa [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para dar formato a una cadena que contiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="b855a-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="b855a-106">La propiedad \[ \# FileKey \] se resuelve en la ruta de acceso completa del archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="b855a-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="b855a-107">Use el archivo de origen para crear el Tutorial.dll de archivo.</span><span class="sxs-lookup"><span data-stu-id="b855a-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="b855a-108">El punto de entrada a este archivo DLL es LaunchTutorial.</span><span class="sxs-lookup"><span data-stu-id="b855a-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="b855a-109">El inicio de la acción personalizada de ejemplo llama a un archivo DLL escrito en C++ y se genera a partir de una secuencia binaria temporal.</span><span class="sxs-lookup"><span data-stu-id="b855a-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="b855a-110">Entre las acciones personalizadas de este tipo se incluyen las constantes de tipo base msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData, que dan un tipo numérico base igual a 1.</span><span class="sxs-lookup"><span data-stu-id="b855a-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="b855a-111">Consulte [acción personalizada tipo 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="b855a-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="b855a-112">Dado que las especificaciones requieren que la instalación continúe si se produce un error en la acción personalizada, el lanzamiento también incluye la constante opcional **msidbCustomActionTypeContinue**, que es 64.</span><span class="sxs-lookup"><span data-stu-id="b855a-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="b855a-113">Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="b855a-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="b855a-114">El tipo numérico total de Launch es 65.</span><span class="sxs-lookup"><span data-stu-id="b855a-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="b855a-115">Continúe [agregando el inicio a las tablas de CustomAction y binarias](adding-launch-to-the-customaction-and-binary-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b855a-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



