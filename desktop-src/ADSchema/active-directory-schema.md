---
title: Esquema de Active Directory (esquema de AD)
description: El esquema de Microsoft Active Directory contiene definiciones formales de cada clase de objeto que se puede crear en un bosque Active Directory.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Esquema de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105656353"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="c22bd-104">Esquema de Active Directory (esquema de AD)</span><span class="sxs-lookup"><span data-stu-id="c22bd-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="c22bd-105">El esquema de Microsoft Active Directory contiene definiciones formales de cada clase de objeto que se puede crear en un bosque Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c22bd-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="c22bd-106">El esquema también contiene definiciones formales de cada atributo que puede existir en un objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c22bd-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="c22bd-107">En esta sección se proporciona la referencia para cada objeto de esquema y se proporciona una breve explicación de los atributos, las clases y otros objetos que componen el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c22bd-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="c22bd-108">La siguiente documentación contiene la referencia de programación para Active Directory esquema.</span><span class="sxs-lookup"><span data-stu-id="c22bd-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="c22bd-109">Si es un usuario final que intenta depurar un error de impresora, intente buscar en el [sitio](https://answers.microsoft.com)de la comunidad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c22bd-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="c22bd-110">Si es un desarrollador que busca información general de Active Directory esquema, consulte los temas de información general sobre el [esquema de Active Directory](/windows/desktop/AD/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="c22bd-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="c22bd-111">Si busca instrucciones de programación para actualizar o modificar el esquema, para obtener más información sobre cómo extender y personalizar el esquema, consulte [extensión del esquema](/windows/desktop/AD/extending-the-schema), así como muchos de los temas de las guías de programación de [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) y [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) .</span><span class="sxs-lookup"><span data-stu-id="c22bd-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="c22bd-112">En cada uno de los temas de referencia hay una sección para cada sistema operativo al que se aplica el tema.</span><span class="sxs-lookup"><span data-stu-id="c22bd-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="c22bd-113">Actualmente se admiten los siguientes sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="c22bd-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="c22bd-114">Plataforma</span><span class="sxs-lookup"><span data-stu-id="c22bd-114">Platform</span></span>                                                      | <span data-ttu-id="c22bd-115">Nombre en el tema</span><span class="sxs-lookup"><span data-stu-id="c22bd-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="c22bd-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c22bd-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="c22bd-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c22bd-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="c22bd-118">Microsoft Active Directory Application Mode (ADAM)</span><span class="sxs-lookup"><span data-stu-id="c22bd-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="c22bd-119">ADAM</span><span class="sxs-lookup"><span data-stu-id="c22bd-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="c22bd-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c22bd-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="c22bd-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c22bd-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="c22bd-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c22bd-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="c22bd-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c22bd-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="c22bd-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c22bd-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="c22bd-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c22bd-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="c22bd-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c22bd-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="c22bd-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c22bd-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="c22bd-128">Si un sistema operativo no aparece en el tema, el tema no se admite en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c22bd-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="c22bd-129">Por ejemplo, si un tema solo muestra Windows Server 2003 y ADAM, el tema no se aplica a Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="c22bd-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="c22bd-130">Las secciones siguientes contienen información detallada sobre los elementos de esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c22bd-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="c22bd-131">Terminología de esquemas Active Directory</span><span class="sxs-lookup"><span data-stu-id="c22bd-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="c22bd-132">Clases</span><span class="sxs-lookup"><span data-stu-id="c22bd-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="c22bd-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="c22bd-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="c22bd-134">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c22bd-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="c22bd-135">Derechos de acceso de control</span><span class="sxs-lookup"><span data-stu-id="c22bd-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="c22bd-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="c22bd-136">RootDSE</span></span>](rootdse.md)

 

