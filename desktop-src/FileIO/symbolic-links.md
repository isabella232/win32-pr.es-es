---
description: Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que apunta se denomina destino.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Vínculos simbólicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688285"
---
# <a name="symbolic-links"></a><span data-ttu-id="50da7-104">Vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="50da7-104">Symbolic Links</span></span>

<span data-ttu-id="50da7-105">Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="50da7-105">A symbolic link is a file-system object that points to another file system object.</span></span> <span data-ttu-id="50da7-106">El objeto al que apunta se denomina destino.</span><span class="sxs-lookup"><span data-stu-id="50da7-106">The object being pointed to is called the target.</span></span>

<span data-ttu-id="50da7-107">Los vínculos simbólicos son transparentes para los usuarios; los vínculos aparecen como archivos o directorios normales y el usuario o la aplicación pueden actuar de la misma manera de igual forma.</span><span class="sxs-lookup"><span data-stu-id="50da7-107">Symbolic links are transparent to users; the links appear as normal files or directories, and can be acted upon by the user or application in exactly the same manner.</span></span>

<span data-ttu-id="50da7-108">Los vínculos simbólicos están diseñados para facilitar la migración y la compatibilidad de aplicaciones con sistemas operativos UNIX.</span><span class="sxs-lookup"><span data-stu-id="50da7-108">Symbolic links are designed to aid in migration and application compatibility with UNIX operating systems.</span></span> <span data-ttu-id="50da7-109">Microsoft ha implementado sus vínculos simbólicos para que funcionen igual que los vínculos de UNIX.</span><span class="sxs-lookup"><span data-stu-id="50da7-109">Microsoft has implemented its symbolic links to function just like UNIX links.</span></span>

<span data-ttu-id="50da7-110">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="50da7-110">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50da7-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="50da7-111">In this section</span></span>



| <span data-ttu-id="50da7-112">Tema</span><span class="sxs-lookup"><span data-stu-id="50da7-112">Topic</span></span>                                                                                                             | <span data-ttu-id="50da7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="50da7-113">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50da7-114">Efectos simbólicos de los vínculos en las funciones del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="50da7-114">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)<br/> | <span data-ttu-id="50da7-115">Cómo afectan los vínculos simbólicos a las funciones de archivo estándar que usan nombres de ruta de acceso para especificar uno o varios archivos.</span><span class="sxs-lookup"><span data-stu-id="50da7-115">How symbolic links affect standard file functions that use path names to specify one or more files.</span></span><br/>                                        |
| [<span data-ttu-id="50da7-116">Consideraciones sobre la programación</span><span class="sxs-lookup"><span data-stu-id="50da7-116">Programming Considerations</span></span>](symbolic-link-programming-considerations.md)<br/>                             | <span data-ttu-id="50da7-117">Consideraciones de programación para trabajar con vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="50da7-117">Programming considerations for working with symbolic links.</span></span><br/>                                                                                |
| [<span data-ttu-id="50da7-118">Crear vínculos simbólicos</span><span class="sxs-lookup"><span data-stu-id="50da7-118">Creating Symbolic Links</span></span>](creating-symbolic-links.md)<br/>                                                 | <span data-ttu-id="50da7-119">Cree vínculos simbólicos que usen una ruta de acceso absoluta o relativa mediante la función [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .</span><span class="sxs-lookup"><span data-stu-id="50da7-119">Create symbolic links that use either an absolute or relative path by using the [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) function.</span></span><br/> |



 

## <a name="supported-operating-systems"></a><span data-ttu-id="50da7-120">Sistemas operativos compatibles</span><span class="sxs-lookup"><span data-stu-id="50da7-120">Supported Operating Systems</span></span>

<span data-ttu-id="50da7-121">Los vínculos simbólicos están disponibles en NTFS a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="50da7-121">Symbolic links are available in NTFS starting with Windows Vista.</span></span>

 

 




