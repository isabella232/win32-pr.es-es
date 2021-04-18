---
description: Define el prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715801"
---
# <a name="macroprefix-element"></a><span data-ttu-id="ad52f-103">elemento macroPrefix</span><span class="sxs-lookup"><span data-stu-id="ad52f-103">macroPrefix element</span></span>

<span data-ttu-id="ad52f-104">Define el prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ad52f-104">Defines the prefix to be used in the generated code for names of macros in the namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="ad52f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ad52f-105">Usage</span></span>

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a><span data-ttu-id="ad52f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad52f-106">Attributes</span></span>

<span data-ttu-id="ad52f-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="ad52f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ad52f-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad52f-108">Child elements</span></span>

<span data-ttu-id="ad52f-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ad52f-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ad52f-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ad52f-110">Parent elements</span></span>



| <span data-ttu-id="ad52f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="ad52f-111">Element</span></span>                                   | <span data-ttu-id="ad52f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad52f-112">Description</span></span>                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ad52f-113">**System.IO**</span><span class="sxs-lookup"><span data-stu-id="ad52f-113">**nameSpace**</span></span>](namespace.md)<br/> | <span data-ttu-id="ad52f-114">Espacio de nombres que se va a utilizar para la generación de código.</span><span class="sxs-lookup"><span data-stu-id="ad52f-114">A namespace to be used for code generation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ad52f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad52f-115">Remarks</span></span>

<span data-ttu-id="ad52f-116">Este elemento invalida el prefijo de URI predeterminado utilizado para las macros generadas.</span><span class="sxs-lookup"><span data-stu-id="ad52f-116">This element overrides the default URI prefix used for generated macros.</span></span> <span data-ttu-id="ad52f-117">Por ejemplo, si el prefijo de la macro es "AV \_ " y el nombre es "sintonizador", la macro generada para el nombre completo será " \_ sintonizador de AV".</span><span class="sxs-lookup"><span data-stu-id="ad52f-117">For example, if the macro prefix is "AV\_" and the name is "Tuner", the macro generated for the qualified name will be "AV\_Tuner".</span></span>

<span data-ttu-id="ad52f-118">De forma predeterminada, el código generado crea un prefijo de macro preferido a partir del URI.</span><span class="sxs-lookup"><span data-stu-id="ad52f-118">By default, the code generated creates a preferred macro prefix from the URI.</span></span>

## <a name="element-information"></a><span data-ttu-id="ad52f-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ad52f-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ad52f-120">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad52f-120">Minimum supported system</span></span><br/> | <span data-ttu-id="ad52f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad52f-121">Windows Vista</span></span> |
| <span data-ttu-id="ad52f-122">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad52f-122">Can be empty</span></span>                        | <span data-ttu-id="ad52f-123">Sí</span><span class="sxs-lookup"><span data-stu-id="ad52f-123">Yes</span></span>           |



 

 




