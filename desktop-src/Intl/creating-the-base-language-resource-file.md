---
description: Crear el archivo de recursos de idioma base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Crear el archivo de recursos de idioma base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083264"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="f44bd-103">Crear el archivo de recursos de idioma base</span><span class="sxs-lookup"><span data-stu-id="f44bd-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="f44bd-104">Los recursos de los elementos de la interfaz de usuario se definen para el idioma básico que admite la aplicación, por ejemplo, Inglés (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="f44bd-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="f44bd-105">Un ejemplo de un archivo de recursos PE de Win32 es un archivo. rc, creado mediante el compilador RC.</span><span class="sxs-lookup"><span data-stu-id="f44bd-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="f44bd-106">Para más información sobre la creación de archivos. rc, consulte [acerca de los archivos de recursos](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="f44bd-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="f44bd-107">Si usa un archivo. RC para los recursos de idioma base, tiene la opción de usar un archivo de configuración de recursos para una representación XML de los datos de configuración de recursos.</span><span class="sxs-lookup"><span data-stu-id="f44bd-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="f44bd-108">Para crear este archivo, consulte [preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="f44bd-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="f44bd-109">También puede usar un archivo PE que no sea de Win32 para definir recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="f44bd-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="f44bd-110">Por ejemplo, puede usar un archivo. XML o. txt para este fin.</span><span class="sxs-lookup"><span data-stu-id="f44bd-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="f44bd-111">Al definir los recursos de idioma base mediante un archivo PE que no es de Win32, no puede usar el compilador RC para la definición de recursos.</span><span class="sxs-lookup"><span data-stu-id="f44bd-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="f44bd-112">En su lugar, defina su propio formato de recursos y la aplicación debe proporcionar su propia funcionalidad para buscar y cargar los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="f44bd-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f44bd-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f44bd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f44bd-114">Preparación de recursos</span><span class="sxs-lookup"><span data-stu-id="f44bd-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="f44bd-115">Preparación de un archivo de configuración de recursos</span><span class="sxs-lookup"><span data-stu-id="f44bd-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
