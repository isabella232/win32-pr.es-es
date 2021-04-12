---
title: Información sobre la versión
description: En este tema se describen las funciones de información de versión.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- recursos, información de versión
- información de versión
- agregar información de versión
- conflictos de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420609"
---
# <a name="about-version-information"></a><span data-ttu-id="2d43e-107">Información sobre la versión</span><span class="sxs-lookup"><span data-stu-id="2d43e-107">About Version Information</span></span>

<span data-ttu-id="2d43e-108">Puede utilizar las funciones de información de versión para determinar dónde debe instalarse un archivo e identificar conflictos con los archivos instalados actualmente.</span><span class="sxs-lookup"><span data-stu-id="2d43e-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="2d43e-109">Estas funciones permiten evitar los problemas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d43e-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="2d43e-110">instalar versiones anteriores de componentes en versiones más recientes</span><span class="sxs-lookup"><span data-stu-id="2d43e-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="2d43e-111">cambiar el idioma en un sistema de lenguaje mixto sin notificación</span><span class="sxs-lookup"><span data-stu-id="2d43e-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="2d43e-112">instalación de varias copias de una biblioteca en directorios diferentes</span><span class="sxs-lookup"><span data-stu-id="2d43e-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="2d43e-113">copiar archivos en directorios de red compartidos por varios usuarios</span><span class="sxs-lookup"><span data-stu-id="2d43e-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="2d43e-114">Las funciones de información de versión permiten a las aplicaciones consultar un recurso de versión en busca de información de archivos y presentar la información en un formato sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="2d43e-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="2d43e-115">Esta información incluye el propósito del archivo, el autor, el número de versión, etc.</span><span class="sxs-lookup"><span data-stu-id="2d43e-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="2d43e-116">Puede agregar información de versión a cualquier archivo que pueda tener recursos de Windows, como archivos dll, archivos ejecutables o archivos de fuentes. fon.</span><span class="sxs-lookup"><span data-stu-id="2d43e-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="2d43e-117">Para agregar la información, cree un [recurso versionInfo](/windows/desktop/menurc/versioninfo-resource) y use el compilador de recursos para compilar el recurso.</span><span class="sxs-lookup"><span data-stu-id="2d43e-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 