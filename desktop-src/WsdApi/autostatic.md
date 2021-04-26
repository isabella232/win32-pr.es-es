---
description: Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: elemento autoStatic
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994932"
---
# <a name="autostatic-element"></a><span data-ttu-id="6ad4b-103">elemento autoStatic</span><span class="sxs-lookup"><span data-stu-id="6ad4b-103">autoStatic element</span></span>

<span data-ttu-id="6ad4b-104">Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="6ad4b-105">Este comportamiento está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="6ad4b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="6ad4b-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="6ad4b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6ad4b-107">Attributes</span></span>

<span data-ttu-id="6ad4b-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6ad4b-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6ad4b-109">Child elements</span></span>

<span data-ttu-id="6ad4b-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6ad4b-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6ad4b-111">Parent elements</span></span>



| <span data-ttu-id="6ad4b-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ad4b-112">Element</span></span>                                     | <span data-ttu-id="6ad4b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ad4b-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ad4b-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="6ad4b-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="6ad4b-115">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6ad4b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ad4b-116">Remarks</span></span>

<span data-ttu-id="6ad4b-117">El **elemento autoStatic** no es necesario y se puede omitir en el archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="6ad4b-118">El elemento se puede usar para deshabilitar la marcación de los campos generados como estáticos o para forzar explícitamente la marcación de determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="6ad4b-119">Los valores posibles son 1 (habilitado, predeterminado) y 0 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="6ad4b-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="6ad4b-120">La **habilitación de autoStatic** puede provocar problemas de compilación en función de cómo se dirija el generador de código a los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="6ad4b-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="6ad4b-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6ad4b-121">Element information</span></span>



| <span data-ttu-id="6ad4b-122">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6ad4b-122">Label</span></span> | <span data-ttu-id="6ad4b-123">Value</span><span class="sxs-lookup"><span data-stu-id="6ad4b-123">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6ad4b-124">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ad4b-124">Minimum supported system</span></span><br/> | <span data-ttu-id="6ad4b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ad4b-125">Windows Vista</span></span> |
| <span data-ttu-id="6ad4b-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6ad4b-126">Can be empty</span></span>                        | <span data-ttu-id="6ad4b-127">Sí</span><span class="sxs-lookup"><span data-stu-id="6ad4b-127">Yes</span></span>           |



 

 




