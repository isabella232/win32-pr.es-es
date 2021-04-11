---
description: Para NLS, ordenación (también conocida como &\# 0034; intercalación&\# 0034;) es la disposición de las cadenas.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordenación (internacionalización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279351"
---
# <a name="sorting"></a><span data-ttu-id="49f13-103">Ordenación</span><span class="sxs-lookup"><span data-stu-id="49f13-103">Sorting</span></span>

<span data-ttu-id="49f13-104">En el caso de NLS, la ordenación (también conocida como "intercalación") es la organización de las cadenas.</span><span class="sxs-lookup"><span data-stu-id="49f13-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="49f13-105">Hay dos tipos de ordenación:</span><span class="sxs-lookup"><span data-stu-id="49f13-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="49f13-106">Ordenación lingüística.</span><span class="sxs-lookup"><span data-stu-id="49f13-106">Linguistic sorting.</span></span> <span data-ttu-id="49f13-107">Organiza las cadenas con características lingüísticas similares en grupos (por orden).</span><span class="sxs-lookup"><span data-stu-id="49f13-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="49f13-108">Ordenación ordinal (no lingüística).</span><span class="sxs-lookup"><span data-stu-id="49f13-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="49f13-109">Organiza las cadenas en una secuencia ordenada.</span><span class="sxs-lookup"><span data-stu-id="49f13-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="49f13-110">La ordenación utiliza las funciones de comparación de cadenas NLS, como [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) y [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), o las funciones de la API "wrapper", como [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), que llaman internamente a las funciones de comparación de cadenas NLS.</span><span class="sxs-lookup"><span data-stu-id="49f13-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="49f13-111">Para obtener más información sobre la implementación de la ordenación en las aplicaciones, vea [controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="49f13-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49f13-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49f13-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f13-113">Acerca de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="49f13-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="49f13-114">Controlar la ordenación en las aplicaciones</span><span class="sxs-lookup"><span data-stu-id="49f13-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="49f13-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="49f13-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="49f13-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="49f13-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
