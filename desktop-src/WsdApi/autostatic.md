---
description: Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: Autostatic (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715813"
---
# <a name="autostatic-element"></a><span data-ttu-id="71678-103">Autostatic (elemento)</span><span class="sxs-lookup"><span data-stu-id="71678-103">autoStatic element</span></span>

<span data-ttu-id="71678-104">Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="71678-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="71678-105">Este comportamiento está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="71678-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="71678-106">Uso</span><span class="sxs-lookup"><span data-stu-id="71678-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="71678-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="71678-107">Attributes</span></span>

<span data-ttu-id="71678-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="71678-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="71678-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71678-109">Child elements</span></span>

<span data-ttu-id="71678-110">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="71678-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="71678-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="71678-111">Parent elements</span></span>



| <span data-ttu-id="71678-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="71678-112">Element</span></span>                                     | <span data-ttu-id="71678-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="71678-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="71678-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="71678-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="71678-115">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="71678-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="71678-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71678-116">Remarks</span></span>

<span data-ttu-id="71678-117">El elemento **Autostatic** no es necesario y se puede omitir en el archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="71678-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="71678-118">El elemento se puede utilizar para deshabilitar la marca de los campos generados como estáticos o para forzar explícitamente la marca de determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="71678-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="71678-119">Los valores posibles son 1 (habilitado, predeterminado) y 0 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="71678-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="71678-120">La habilitación de **Autostatic** puede producir problemas de compilación en función de cómo se dirija el generador de código a los datos de salida.</span><span class="sxs-lookup"><span data-stu-id="71678-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="71678-121">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="71678-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="71678-122">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71678-122">Minimum supported system</span></span><br/> | <span data-ttu-id="71678-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71678-123">Windows Vista</span></span> |
| <span data-ttu-id="71678-124">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="71678-124">Can be empty</span></span>                        | <span data-ttu-id="71678-125">Sí</span><span class="sxs-lookup"><span data-stu-id="71678-125">Yes</span></span>           |



 

 




