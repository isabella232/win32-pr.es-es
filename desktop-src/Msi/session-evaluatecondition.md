---
description: El método EvaluateCondition del objeto de sesión evalúa una expresión lógica que contiene símbolos y valores. Este método usa la función MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Método Session. EvaluateCondition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680409"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="976e7-104">Método Session. EvaluateCondition</span><span class="sxs-lookup"><span data-stu-id="976e7-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="976e7-105">El método **EvaluateCondition** del objeto de [**sesión**](session-object.md) evalúa una expresión lógica que contiene símbolos y valores.</span><span class="sxs-lookup"><span data-stu-id="976e7-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="976e7-106">Este método usa la función [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="976e7-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="976e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="976e7-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="976e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="976e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976e7-109">*condition*</span><span class="sxs-lookup"><span data-stu-id="976e7-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="976e7-110">Cadena requerida que contiene la expresión lógica.</span><span class="sxs-lookup"><span data-stu-id="976e7-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="976e7-111">Para obtener más información, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="976e7-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976e7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="976e7-112">Return value</span></span>

<span data-ttu-id="976e7-113">Este método devuelve un entero que indica la evaluación de la condición.</span><span class="sxs-lookup"><span data-stu-id="976e7-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="976e7-114">Constante</span><span class="sxs-lookup"><span data-stu-id="976e7-114">Constant</span></span>                  | <span data-ttu-id="976e7-115">Value</span><span class="sxs-lookup"><span data-stu-id="976e7-115">Value</span></span> | <span data-ttu-id="976e7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="976e7-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="976e7-117">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="976e7-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="976e7-118">0</span><span class="sxs-lookup"><span data-stu-id="976e7-118">0</span></span>     | <span data-ttu-id="976e7-119">La condición se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="976e7-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="976e7-120">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="976e7-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="976e7-121">1</span><span class="sxs-lookup"><span data-stu-id="976e7-121">1</span></span>     | <span data-ttu-id="976e7-122">La condición se evalúa como true.</span><span class="sxs-lookup"><span data-stu-id="976e7-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="976e7-123">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="976e7-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="976e7-124">2</span><span class="sxs-lookup"><span data-stu-id="976e7-124">2</span></span>     | <span data-ttu-id="976e7-125">No se proporciona una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="976e7-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="976e7-126">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="976e7-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="976e7-127">3</span><span class="sxs-lookup"><span data-stu-id="976e7-127">3</span></span>     | <span data-ttu-id="976e7-128">La condición contiene un error de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="976e7-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="976e7-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="976e7-129">Remarks</span></span>

<span data-ttu-id="976e7-130">Las expresiones condicionales se pueden usar para comparar los Estados de las características y los componentes.</span><span class="sxs-lookup"><span data-stu-id="976e7-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="976e7-131">En la tabla siguiente se muestran los Estados de características y componentes que usa el método EvaluateCondition.</span><span class="sxs-lookup"><span data-stu-id="976e7-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="976e7-132">Estado</span><span class="sxs-lookup"><span data-stu-id="976e7-132">State</span></span>                 | <span data-ttu-id="976e7-133">Value</span><span class="sxs-lookup"><span data-stu-id="976e7-133">Value</span></span> | <span data-ttu-id="976e7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="976e7-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="976e7-135">Null</span><span class="sxs-lookup"><span data-stu-id="976e7-135">Null</span></span>                  | <span data-ttu-id="976e7-136">Null</span><span class="sxs-lookup"><span data-stu-id="976e7-136">Null</span></span>  | <span data-ttu-id="976e7-137">No se realizó ninguna acción en la característica o componente.</span><span class="sxs-lookup"><span data-stu-id="976e7-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="976e7-138">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="976e7-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="976e7-139">2</span><span class="sxs-lookup"><span data-stu-id="976e7-139">2</span></span>     | <span data-ttu-id="976e7-140">La característica o componente no está presente.</span><span class="sxs-lookup"><span data-stu-id="976e7-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="976e7-141">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="976e7-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="976e7-142">3</span><span class="sxs-lookup"><span data-stu-id="976e7-142">3</span></span>     | <span data-ttu-id="976e7-143">La característica o componente está instalado en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="976e7-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="976e7-144">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="976e7-144">msiInstallStateSource</span></span> | <span data-ttu-id="976e7-145">4</span><span class="sxs-lookup"><span data-stu-id="976e7-145">4</span></span>     | <span data-ttu-id="976e7-146">La característica o componente está instalado para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="976e7-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="976e7-147">Los Estados no se establecen hasta que se llama al método [**SetInstallLevel**](session-setinstalllevel.md) , ya sea directamente o mediante la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="976e7-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="976e7-148">Por lo tanto, la comprobación de estado solo es útil en una expresión condicional en una tabla de secuencia de acciones.</span><span class="sxs-lookup"><span data-stu-id="976e7-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="976e7-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="976e7-149">Requirements</span></span>



| <span data-ttu-id="976e7-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="976e7-150">Requirement</span></span> | <span data-ttu-id="976e7-151">Value</span><span class="sxs-lookup"><span data-stu-id="976e7-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="976e7-152">Versión</span><span class="sxs-lookup"><span data-stu-id="976e7-152">Version</span></span><br/> | <span data-ttu-id="976e7-153">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="976e7-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="976e7-154">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="976e7-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="976e7-155">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="976e7-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="976e7-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="976e7-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="976e7-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="976e7-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="976e7-158">IID</span><span class="sxs-lookup"><span data-stu-id="976e7-158">IID</span></span><br/>     | <span data-ttu-id="976e7-159">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="976e7-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="976e7-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="976e7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976e7-161">Sintaxis de la instrucción condicional</span><span class="sxs-lookup"><span data-stu-id="976e7-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




