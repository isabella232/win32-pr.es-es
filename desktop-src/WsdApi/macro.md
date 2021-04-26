---
description: Define el texto o CDATA que el elemento include va a reutilizar.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994332"
---
# <a name="macro-element"></a><span data-ttu-id="ba98a-103">macro, elemento</span><span class="sxs-lookup"><span data-stu-id="ba98a-103">macro element</span></span>

<span data-ttu-id="ba98a-104">Define el texto o CDATA que va a reutilizar el [**elemento include.**](include.md)</span><span class="sxs-lookup"><span data-stu-id="ba98a-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="ba98a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ba98a-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="ba98a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba98a-106">Attributes</span></span>



| <span data-ttu-id="ba98a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="ba98a-107">Attribute</span></span>           | <span data-ttu-id="ba98a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba98a-108">Type</span></span>                         | <span data-ttu-id="ba98a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ba98a-109">Required</span></span>       | <span data-ttu-id="ba98a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba98a-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="ba98a-111">**name**</span><span class="sxs-lookup"><span data-stu-id="ba98a-111">**name**</span></span><br/> | <span data-ttu-id="ba98a-112">cadena \_ de caracteres</span><span class="sxs-lookup"><span data-stu-id="ba98a-112">character\_string</span></span><br/> | <span data-ttu-id="ba98a-113">Sí</span><span class="sxs-lookup"><span data-stu-id="ba98a-113">Yes</span></span><br/> | <span data-ttu-id="ba98a-114">Nombre de la macro.</span><span class="sxs-lookup"><span data-stu-id="ba98a-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ba98a-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba98a-115">Child elements</span></span>

<span data-ttu-id="ba98a-116">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ba98a-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ba98a-117">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ba98a-117">Parent elements</span></span>



| <span data-ttu-id="ba98a-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba98a-118">Element</span></span>                                     | <span data-ttu-id="ba98a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba98a-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba98a-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="ba98a-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="ba98a-121">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ba98a-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ba98a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba98a-122">Remarks</span></span>

<span data-ttu-id="ba98a-123">WsdCodeGen define una macro denominada **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="ba98a-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="ba98a-124">Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.</span><span class="sxs-lookup"><span data-stu-id="ba98a-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="ba98a-125">En el xml siguiente se muestra cómo incluir la macro **DoNotModify.**</span><span class="sxs-lookup"><span data-stu-id="ba98a-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="ba98a-126">Este XML se puede agregar a un archivo de configuración XML para WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="ba98a-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="ba98a-127">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ba98a-127">Element information</span></span>



| <span data-ttu-id="ba98a-128">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="ba98a-128">Label</span></span> | <span data-ttu-id="ba98a-129">Value</span><span class="sxs-lookup"><span data-stu-id="ba98a-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="ba98a-130">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba98a-130">Minimum supported system</span></span><br/> | <span data-ttu-id="ba98a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba98a-131">Windows Vista</span></span> |
| <span data-ttu-id="ba98a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba98a-132">Can be empty</span></span>                        | <span data-ttu-id="ba98a-133">Sí</span><span class="sxs-lookup"><span data-stu-id="ba98a-133">Yes</span></span>           |



 

 




