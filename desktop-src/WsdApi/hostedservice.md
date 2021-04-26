---
description: Define un servicio que se va a hospedar en una función del generador de host.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994792"
---
# <a name="hostedservice-element"></a><span data-ttu-id="6ad51-103">elemento hostedService</span><span class="sxs-lookup"><span data-stu-id="6ad51-103">hostedService element</span></span>

<span data-ttu-id="6ad51-104">Define un servicio que se va a hospedar en una función del generador de host.</span><span class="sxs-lookup"><span data-stu-id="6ad51-104">Defines a service to be hosted in a host builder function.</span></span>

## <a name="usage"></a><span data-ttu-id="6ad51-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6ad51-105">Usage</span></span>

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a><span data-ttu-id="6ad51-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ad51-106">Attributes</span></span>

<span data-ttu-id="6ad51-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="6ad51-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6ad51-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ad51-108">Child elements</span></span>



| <span data-ttu-id="6ad51-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ad51-109">Element</span></span>                                     | <span data-ttu-id="6ad51-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ad51-110">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ad51-111">**Codename**</span><span class="sxs-lookup"><span data-stu-id="6ad51-111">**codeName**</span></span>](codename.md)<br/>     | <span data-ttu-id="6ad51-112">Especifica el nombre que se usará para el tipo de puerto en el código generado.</span><span class="sxs-lookup"><span data-stu-id="6ad51-112">Specifies the name to be used for the port type in the generated code.</span></span> <span data-ttu-id="6ad51-113">De forma predeterminada, el nombre del código se genera a partir del nombre completo del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="6ad51-113">By default, the code name is generated from the port type's qualified name.</span></span><br/> <br/> |
| [<span data-ttu-id="6ad51-114">**portType**</span><span class="sxs-lookup"><span data-stu-id="6ad51-114">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="6ad51-115">Tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="6ad51-115">Port type for which code is to be generated.</span></span><br/> <br/>                                                                                                       |
| [<span data-ttu-id="6ad51-116">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="6ad51-116">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="6ad51-117">Nombre de clase que se generará a partir de la función de generador.</span><span class="sxs-lookup"><span data-stu-id="6ad51-117">Class name to generate from builder function.</span></span><br/> <br/>                                                                                                      |
| [<span data-ttu-id="6ad51-118">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="6ad51-118">**ServiceID**</span></span>](serviceid.md)<br/>   | <span data-ttu-id="6ad51-119">URI que representa el identificador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ad51-119">A URI that represents the service identifier.</span></span><br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="6ad51-120">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ad51-120">Child element sequence</span></span>

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a><span data-ttu-id="6ad51-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6ad51-121">Parent elements</span></span>



| <span data-ttu-id="6ad51-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ad51-122">Element</span></span>                         | <span data-ttu-id="6ad51-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ad51-123">Description</span></span>                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="6ad51-124">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6ad51-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6ad51-125">Especificación del archivo de salida para el generador de código.</span><span class="sxs-lookup"><span data-stu-id="6ad51-125">The output file specification for the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="6ad51-126">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6ad51-126">Element information</span></span>



| <span data-ttu-id="6ad51-127">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6ad51-127">Label</span></span> | <span data-ttu-id="6ad51-128">Value</span><span class="sxs-lookup"><span data-stu-id="6ad51-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6ad51-129">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ad51-129">Minimum supported system</span></span><br/> | <span data-ttu-id="6ad51-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ad51-130">Windows Vista</span></span> |
| <span data-ttu-id="6ad51-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ad51-131">Can be empty</span></span>                        | <span data-ttu-id="6ad51-132">No</span><span class="sxs-lookup"><span data-stu-id="6ad51-132">No</span></span>            |



 

 




