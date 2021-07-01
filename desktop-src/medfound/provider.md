---
description: Especifica un proveedor de seguimiento (ETW o WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118450"
---
# <a name="provider-element"></a><span data-ttu-id="50d37-103">provider (elemento)</span><span class="sxs-lookup"><span data-stu-id="50d37-103">provider element</span></span>

<span data-ttu-id="50d37-104">Especifica un proveedor de seguimiento (ETW o WPP) para [MFTrace.](mftrace.md)</span><span class="sxs-lookup"><span data-stu-id="50d37-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="50d37-105">Uso</span><span class="sxs-lookup"><span data-stu-id="50d37-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="50d37-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="50d37-106">Attributes</span></span>



| <span data-ttu-id="50d37-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="50d37-107">Attribute</span></span>            | <span data-ttu-id="50d37-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="50d37-108">Type</span></span>             | <span data-ttu-id="50d37-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="50d37-109">Required</span></span>       | <span data-ttu-id="50d37-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="50d37-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="50d37-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="50d37-111">**ID**</span></span><br/>    | <span data-ttu-id="50d37-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="50d37-112">CDATA</span></span><br/> | <span data-ttu-id="50d37-113">Sí</span><span class="sxs-lookup"><span data-stu-id="50d37-113">Yes</span></span><br/> | <span data-ttu-id="50d37-114">Nombre o GUID del proveedor.</span><span class="sxs-lookup"><span data-stu-id="50d37-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="50d37-115">**level**</span><span class="sxs-lookup"><span data-stu-id="50d37-115">**level**</span></span><br/> | <span data-ttu-id="50d37-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="50d37-116">CDATA</span></span><br/> | <span data-ttu-id="50d37-117">Sí</span><span class="sxs-lookup"><span data-stu-id="50d37-117">Yes</span></span><br/> | <span data-ttu-id="50d37-118">Nivel de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="50d37-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="50d37-119">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50d37-119">Child elements</span></span>



| <span data-ttu-id="50d37-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="50d37-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="50d37-121">**Palabra clave**</span><span class="sxs-lookup"><span data-stu-id="50d37-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="50d37-122">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="50d37-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="50d37-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="50d37-123">Parent elements</span></span>



| <span data-ttu-id="50d37-124">Elemento</span><span class="sxs-lookup"><span data-stu-id="50d37-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="50d37-125">**Proveedores**</span><span class="sxs-lookup"><span data-stu-id="50d37-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="50d37-126">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="50d37-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="50d37-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="50d37-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="50d37-128">No</span><span class="sxs-lookup"><span data-stu-id="50d37-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="50d37-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50d37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d37-130">Archivo de configuración de MFTrace</span><span class="sxs-lookup"><span data-stu-id="50d37-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




