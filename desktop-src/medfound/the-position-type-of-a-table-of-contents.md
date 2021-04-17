---
description: El tipo de posición de una tabla de contenido
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: El tipo de posición de una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696882"
---
# <a name="the-position-type-of-a-table-of-contents"></a><span data-ttu-id="a18e3-103">El tipo de posición de una tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="a18e3-103">The Position Type of a Table of Contents</span></span>

<span data-ttu-id="a18e3-104">Algunos métodos de la interfaz [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) tienen un parámetro denominado *enumTocPosType* que tiene un tipo de [**tipo de \_ pos \_ de TDC de enumeración**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span><span class="sxs-lookup"><span data-stu-id="a18e3-104">Some methods of the [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface have a parameter named *enumTocPosType* that has a type of [**enum TOC\_POS\_TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type).</span></span> <span data-ttu-id="a18e3-105">Este parámetro especifica la posición en un archivo multimedia donde se almacena una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="a18e3-105">This parameter specifies the position in a media file where a table of contents is stored.</span></span> <span data-ttu-id="a18e3-106">La intención era que la tabla de contenido podía almacenarse en el encabezado de archivo o en el cuerpo del archivo como un objeto de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a18e3-106">The intent was that the table of contents could be stored either in the file header or in the body of the file as a top level object.</span></span> <span data-ttu-id="a18e3-107">Esta funcionalidad no se ha implementado todavía.</span><span class="sxs-lookup"><span data-stu-id="a18e3-107">This functionality has not, as yet, been implemented.</span></span>

<span data-ttu-id="a18e3-108">Actualmente, las tablas de contenido solo se pueden almacenar como objetos de nivel superior, por lo que siempre debe establecer el parámetro *enumTocPosType* en el **TOPLEVELOBJECT de \_ pos \_ de TDC**.</span><span class="sxs-lookup"><span data-stu-id="a18e3-108">Currently, tables of contents can only be stored as top level objects, so you must always set the *enumTocPosType* parameter to **TOC\_POS\_TOPLEVELOBJECT**.</span></span> <span data-ttu-id="a18e3-109">Si establece *enumTocPosType* en el **\_ \_ inencabezado de pos de TDC**, el método devolverá **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="a18e3-109">If you set *enumTocPosType* to **TOC\_POS\_INHEADER**, the method will return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="a18e3-110">Los métodos siguientes tienen un parámetro *enumTocPosType* .</span><span class="sxs-lookup"><span data-stu-id="a18e3-110">The following methods have an *enumTocPosType* parameter.</span></span>

-   [<span data-ttu-id="a18e3-111">**GetTocCount**</span><span class="sxs-lookup"><span data-stu-id="a18e3-111">**GetTocCount**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [<span data-ttu-id="a18e3-112">**GetTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="a18e3-112">**GetTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [<span data-ttu-id="a18e3-113">**GetTocByType**</span><span class="sxs-lookup"><span data-stu-id="a18e3-113">**GetTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [<span data-ttu-id="a18e3-114">**AddToc**</span><span class="sxs-lookup"><span data-stu-id="a18e3-114">**AddToc**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [<span data-ttu-id="a18e3-115">**RemoveTocByIndex**</span><span class="sxs-lookup"><span data-stu-id="a18e3-115">**RemoveTocByIndex**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [<span data-ttu-id="a18e3-116">**RemoveTocByType**</span><span class="sxs-lookup"><span data-stu-id="a18e3-116">**RemoveTocByType**</span></span>](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a><span data-ttu-id="a18e3-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a18e3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a18e3-118">Guía de programación del analizador de tabla de contenido</span><span class="sxs-lookup"><span data-stu-id="a18e3-118">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



