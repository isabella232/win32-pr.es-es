---
description: Especifica una palabra clave para un proveedor MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119380"
---
# <a name="keyword-element"></a><span data-ttu-id="b6b1a-103">elemento keyword</span><span class="sxs-lookup"><span data-stu-id="b6b1a-103">keyword element</span></span>

<span data-ttu-id="b6b1a-104">Especifica una palabra clave para un [proveedor MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="b6b1a-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="b6b1a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b6b1a-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="b6b1a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6b1a-106">Attributes</span></span>



| <span data-ttu-id="b6b1a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6b1a-107">Attribute</span></span>         | <span data-ttu-id="b6b1a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6b1a-108">Type</span></span>             | <span data-ttu-id="b6b1a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="b6b1a-109">Required</span></span>       | <span data-ttu-id="b6b1a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6b1a-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="b6b1a-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="b6b1a-111">**ID**</span></span><br/> | <span data-ttu-id="b6b1a-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="b6b1a-112">CDATA</span></span><br/> | <span data-ttu-id="b6b1a-113">Sí</span><span class="sxs-lookup"><span data-stu-id="b6b1a-113">Yes</span></span><br/> | <span data-ttu-id="b6b1a-114">Nombre o máscara de la palabra clave</span><span class="sxs-lookup"><span data-stu-id="b6b1a-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="b6b1a-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6b1a-115">Child elements</span></span>

<span data-ttu-id="b6b1a-116">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b6b1a-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b6b1a-117">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b6b1a-117">Parent elements</span></span>

| <span data-ttu-id="b6b1a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6b1a-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="b6b1a-119">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="b6b1a-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="b6b1a-120">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="b6b1a-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="b6b1a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6b1a-121">Remarks</span></span>

<span data-ttu-id="b6b1a-122">Para el [**elemento mfdetours,**](mfdetours.md) las palabras clave válidas se enumeran en el tema Palabras clave [de MFTrace](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="b6b1a-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="b6b1a-123">Para el [**elemento provider,**](provider.md) las palabras clave dependen del proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="b6b1a-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="b6b1a-124">Puede usar la utilidad Wevtutil.exe para enumerar las palabras clave de un proveedor determinado.</span><span class="sxs-lookup"><span data-stu-id="b6b1a-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="b6b1a-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b6b1a-125">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="b6b1a-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6b1a-126">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="b6b1a-127">Sí</span><span class="sxs-lookup"><span data-stu-id="b6b1a-127">Yes</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="b6b1a-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b6b1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b1a-129">Archivo de configuración de MFTrace</span><span class="sxs-lookup"><span data-stu-id="b6b1a-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="b6b1a-130">Palabras clave de MFTrace</span><span class="sxs-lookup"><span data-stu-id="b6b1a-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




