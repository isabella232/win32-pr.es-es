---
description: El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652618"
---
# <a name="anypath"></a><span data-ttu-id="c2220-103">AnyPath</span><span class="sxs-lookup"><span data-stu-id="c2220-103">AnyPath</span></span>

<span data-ttu-id="c2220-104">El tipo de datos AnyPath es una cadena de texto que contiene una ruta de acceso completa o una ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="c2220-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="c2220-105">Al especificar una ruta de acceso relativa, puede incluir un nombre de archivo largo con el nombre de archivo corto separando los nombres corto y largo con una barra vertical ( \| ).</span><span class="sxs-lookup"><span data-stu-id="c2220-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="c2220-106">Tenga en cuenta que no puede especificar varios niveles de un directorio o rutas de acceso completas de esta manera.</span><span class="sxs-lookup"><span data-stu-id="c2220-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="c2220-107">La ruta de acceso puede contener propiedades entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="c2220-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="c2220-108">Ejemplos de datos de AnyPath válidos:</span><span class="sxs-lookup"><span data-stu-id="c2220-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="c2220-109">\\\\\\recurso compartido de servidor \\ temporal</span><span class="sxs-lookup"><span data-stu-id="c2220-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="c2220-110">c: \\ Temp</span><span class="sxs-lookup"><span data-stu-id="c2220-110">c:\\temp</span></span>
-   <span data-ttu-id="c2220-111">\\temperatura</span><span class="sxs-lookup"><span data-stu-id="c2220-111">\\temp</span></span>
-   <span data-ttu-id="c2220-112">Project ~ 1 \| Estado del proyecto</span><span class="sxs-lookup"><span data-stu-id="c2220-112">projec~1\|Project Status</span></span>

<span data-ttu-id="c2220-113">Ejemplos de datos de AnyPath no válidos:</span><span class="sxs-lookup"><span data-stu-id="c2220-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="c2220-114">c: \\ temp \\ Project ~ 1 \| c: \\ temp un \\ Estado de proyecto</span><span class="sxs-lookup"><span data-stu-id="c2220-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="c2220-115">\\Temp \\ Project ~ 1 \| \\ temp un \\ Estado de proyecto</span><span class="sxs-lookup"><span data-stu-id="c2220-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



