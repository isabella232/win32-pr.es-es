---
description: Genera funciones para crear servidores proxy con tipo.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996472"
---
# <a name="proxybuilderimplementations-element"></a><span data-ttu-id="2c15e-103">elemento proxyBuilderImplementations</span><span class="sxs-lookup"><span data-stu-id="2c15e-103">proxyBuilderImplementations element</span></span>

<span data-ttu-id="2c15e-104">Genera funciones para crear servidores proxy con tipo.</span><span class="sxs-lookup"><span data-stu-id="2c15e-104">Generates functions to create typed proxies.</span></span>

## <a name="usage"></a><span data-ttu-id="2c15e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="2c15e-105">Usage</span></span>

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a><span data-ttu-id="2c15e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="2c15e-106">Attributes</span></span>

<span data-ttu-id="2c15e-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="2c15e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2c15e-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c15e-108">Child elements</span></span>



| <span data-ttu-id="2c15e-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c15e-109">Element</span></span>                                     | <span data-ttu-id="2c15e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c15e-110">Description</span></span>                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c15e-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="2c15e-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="2c15e-112">Nombre que se va a usar para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="2c15e-112">The name to be used for the port type in the generated code.</span></span> <span data-ttu-id="2c15e-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="2c15e-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="2c15e-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="2c15e-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="2c15e-115">Tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="2c15e-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                             |
| [<span data-ttu-id="2c15e-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="2c15e-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="2c15e-117">Nombre de clase que se generará a partir de la función del generador de proxy.</span><span class="sxs-lookup"><span data-stu-id="2c15e-117">Class name to generate from the proxy builder function.</span></span><br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="2c15e-118">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2c15e-118">Child element sequence</span></span>

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a><span data-ttu-id="2c15e-119">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="2c15e-119">Parent elements</span></span>



| <span data-ttu-id="2c15e-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c15e-120">Element</span></span>                         | <span data-ttu-id="2c15e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c15e-121">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="2c15e-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2c15e-122">**file**</span></span>](file.md)<br/> | <span data-ttu-id="2c15e-123">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="2c15e-123">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="2c15e-124">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="2c15e-124">Element information</span></span>



| <span data-ttu-id="2c15e-125">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="2c15e-125">Label</span></span> | <span data-ttu-id="2c15e-126">Value</span><span class="sxs-lookup"><span data-stu-id="2c15e-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="2c15e-127">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c15e-127">Minimum supported system</span></span><br/> | <span data-ttu-id="2c15e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c15e-128">Windows Vista</span></span> |
| <span data-ttu-id="2c15e-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2c15e-129">Can be empty</span></span>                        | <span data-ttu-id="2c15e-130">No</span><span class="sxs-lookup"><span data-stu-id="2c15e-130">No</span></span>            |



 

 




