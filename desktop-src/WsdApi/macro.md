---
description: Define el texto o el CDATA que va a reutilizar el elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277116"
---
# <a name="macro-element"></a><span data-ttu-id="63cf1-103">elemento macro</span><span class="sxs-lookup"><span data-stu-id="63cf1-103">macro element</span></span>

<span data-ttu-id="63cf1-104">Define el texto o el CDATA que va a reutilizar el elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="63cf1-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="63cf1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="63cf1-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="63cf1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="63cf1-106">Attributes</span></span>



| <span data-ttu-id="63cf1-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="63cf1-107">Attribute</span></span>           | <span data-ttu-id="63cf1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="63cf1-108">Type</span></span>                         | <span data-ttu-id="63cf1-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="63cf1-109">Required</span></span>       | <span data-ttu-id="63cf1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="63cf1-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="63cf1-111">**name**</span><span class="sxs-lookup"><span data-stu-id="63cf1-111">**name**</span></span><br/> | <span data-ttu-id="63cf1-112">cadena de caracteres \_</span><span class="sxs-lookup"><span data-stu-id="63cf1-112">character\_string</span></span><br/> | <span data-ttu-id="63cf1-113">Sí</span><span class="sxs-lookup"><span data-stu-id="63cf1-113">Yes</span></span><br/> | <span data-ttu-id="63cf1-114">Nombre de la macro.</span><span class="sxs-lookup"><span data-stu-id="63cf1-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="63cf1-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63cf1-115">Child elements</span></span>

<span data-ttu-id="63cf1-116">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="63cf1-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="63cf1-117">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="63cf1-117">Parent elements</span></span>



| <span data-ttu-id="63cf1-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="63cf1-118">Element</span></span>                                     | <span data-ttu-id="63cf1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="63cf1-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="63cf1-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="63cf1-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="63cf1-121">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="63cf1-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="63cf1-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63cf1-122">Remarks</span></span>

<span data-ttu-id="63cf1-123">WsdCodeGen define una macro denominada **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="63cf1-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="63cf1-124">Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.</span><span class="sxs-lookup"><span data-stu-id="63cf1-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="63cf1-125">El siguiente XML muestra cómo incluir la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="63cf1-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="63cf1-126">Este XML se puede Agregar a un archivo de configuración XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="63cf1-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="63cf1-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="63cf1-127">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="63cf1-128">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63cf1-128">Minimum supported system</span></span><br/> | <span data-ttu-id="63cf1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63cf1-129">Windows Vista</span></span> |
| <span data-ttu-id="63cf1-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63cf1-130">Can be empty</span></span>                        | <span data-ttu-id="63cf1-131">Sí</span><span class="sxs-lookup"><span data-stu-id="63cf1-131">Yes</span></span>           |



 

 




