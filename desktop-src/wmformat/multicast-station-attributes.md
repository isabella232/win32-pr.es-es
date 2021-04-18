---
title: Atributos de la estación de multidifusión
description: Atributos de la estación de multidifusión
ms.assetid: 24b81ccb-4030-49a4-802c-5b45f7dd5950
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, estación de multidifusión
- atributos de la estación de multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618ffa645055bf10a9247272d57c7e3f76853c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714249"
---
# <a name="multicast-station-attributes"></a><span data-ttu-id="7cb84-108">Atributos de la estación de multidifusión</span><span class="sxs-lookup"><span data-stu-id="7cb84-108">Multicast Station Attributes</span></span>

<span data-ttu-id="7cb84-109">Cuando un archivo se transmite desde una estación de multidifusión, la estación puede imponer algunos atributos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="7cb84-109">When a file is streaming from a multicast station, the station can impose some attributes on the file.</span></span> <span data-ttu-id="7cb84-110">Estos atributos, que se enumeran en la tabla siguiente, no se almacenan realmente en el archivo y solo están disponibles cuando el archivo se transmite por secuencias.</span><span class="sxs-lookup"><span data-stu-id="7cb84-110">These attributes, listed in the following table, are not actually stored in the file and are only available when the file is streaming.</span></span> <span data-ttu-id="7cb84-111">Contienen información sobre la estación y suelen ser idénticas para todo el contenido de la estación.</span><span class="sxs-lookup"><span data-stu-id="7cb84-111">They contain information about the station and would typically be identical for all content from the station.</span></span>



| <span data-ttu-id="7cb84-112">Atributo de estación de multidifusión</span><span class="sxs-lookup"><span data-stu-id="7cb84-112">Multicast station attribute</span></span>                 | <span data-ttu-id="7cb84-113">Identificador global</span><span class="sxs-lookup"><span data-stu-id="7cb84-113">Global identifier</span></span>      | <span data-ttu-id="7cb84-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7cb84-114">Data type</span></span>             |
|---------------------------------------------|------------------------|-----------------------|
| [<span data-ttu-id="7cb84-115">**\_Dirección NSC**</span><span class="sxs-lookup"><span data-stu-id="7cb84-115">**NSC\_Address**</span></span>](nsc-address.md)         | <span data-ttu-id="7cb84-116">g \_ wszWMNSCAddress</span><span class="sxs-lookup"><span data-stu-id="7cb84-116">g\_wszWMNSCAddress</span></span>     | <span data-ttu-id="7cb84-117">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-117">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="7cb84-118">**Descripción de NSC \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-118">**NSC\_Description**</span></span>](nsc-description.md) | <span data-ttu-id="7cb84-119">g \_ wszWMNSCDescription</span><span class="sxs-lookup"><span data-stu-id="7cb84-119">g\_wszWMNSCDescription</span></span> | <span data-ttu-id="7cb84-120">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-120">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="7cb84-121">**\_Correo electrónico NSC**</span><span class="sxs-lookup"><span data-stu-id="7cb84-121">**NSC\_Email**</span></span>](nsc-email.md)             | <span data-ttu-id="7cb84-122">g \_ wszWMNSCEmail</span><span class="sxs-lookup"><span data-stu-id="7cb84-122">g\_wszWMNSCEmail</span></span>       | <span data-ttu-id="7cb84-123">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-123">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="7cb84-124">**\_Nombre NSC**</span><span class="sxs-lookup"><span data-stu-id="7cb84-124">**NSC\_Name**</span></span>](nsc-name.md)               | <span data-ttu-id="7cb84-125">g \_ wszWMNSCName</span><span class="sxs-lookup"><span data-stu-id="7cb84-125">g\_wszWMNSCName</span></span>        | <span data-ttu-id="7cb84-126">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-126">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="7cb84-127">**\_Teléfono NSC**</span><span class="sxs-lookup"><span data-stu-id="7cb84-127">**NSC\_Phone**</span></span>](nsc-phone.md)             | <span data-ttu-id="7cb84-128">g \_ wszWMNSCPhone</span><span class="sxs-lookup"><span data-stu-id="7cb84-128">g\_wszWMNSCPhone</span></span>       | <span data-ttu-id="7cb84-129">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="7cb84-129">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7cb84-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cb84-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb84-131">**Atributos por tipo**</span><span class="sxs-lookup"><span data-stu-id="7cb84-131">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="7cb84-132">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="7cb84-132">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




