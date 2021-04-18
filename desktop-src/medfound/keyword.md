---
description: Especifica una palabra clave para un proveedor MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707015"
---
# <a name="keyword-element"></a><span data-ttu-id="45a40-103">elemento keyword</span><span class="sxs-lookup"><span data-stu-id="45a40-103">keyword element</span></span>

<span data-ttu-id="45a40-104">Especifica una palabra clave para un proveedor [MFTrace](mftrace.md) .</span><span class="sxs-lookup"><span data-stu-id="45a40-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="45a40-105">Uso</span><span class="sxs-lookup"><span data-stu-id="45a40-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="45a40-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="45a40-106">Attributes</span></span>



| <span data-ttu-id="45a40-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="45a40-107">Attribute</span></span>         | <span data-ttu-id="45a40-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="45a40-108">Type</span></span>             | <span data-ttu-id="45a40-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="45a40-109">Required</span></span>       | <span data-ttu-id="45a40-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="45a40-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="45a40-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="45a40-111">**ID**</span></span><br/> | <span data-ttu-id="45a40-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="45a40-112">CDATA</span></span><br/> | <span data-ttu-id="45a40-113">Sí</span><span class="sxs-lookup"><span data-stu-id="45a40-113">Yes</span></span><br/> | <span data-ttu-id="45a40-114">El nombre o la máscara de la palabra clave</span><span class="sxs-lookup"><span data-stu-id="45a40-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="45a40-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="45a40-115">Child elements</span></span>

<span data-ttu-id="45a40-116">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="45a40-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="45a40-117">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="45a40-117">Parent elements</span></span>



| <span data-ttu-id="45a40-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="45a40-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="45a40-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="45a40-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="45a40-120">**presta**</span><span class="sxs-lookup"><span data-stu-id="45a40-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="45a40-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45a40-121">Remarks</span></span>

<span data-ttu-id="45a40-122">En el caso del elemento [**mfdetours**](mfdetours.md) , se enumeran las palabras clave válidas en el tema palabras clave de [MFTrace](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="45a40-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="45a40-123">En el caso del elemento [**Provider**](provider.md) , las palabras clave dependen del proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="45a40-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="45a40-124">Puede usar la utilidad Wevtutil.exe para mostrar las palabras clave de un proveedor determinado.</span><span class="sxs-lookup"><span data-stu-id="45a40-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="45a40-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="45a40-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="45a40-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="45a40-126">Can be empty</span></span> | <span data-ttu-id="45a40-127">Sí</span><span class="sxs-lookup"><span data-stu-id="45a40-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="45a40-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45a40-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a40-129">Archivo de configuración MFTrace</span><span class="sxs-lookup"><span data-stu-id="45a40-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="45a40-130">Palabras clave de MFTrace</span><span class="sxs-lookup"><span data-stu-id="45a40-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




