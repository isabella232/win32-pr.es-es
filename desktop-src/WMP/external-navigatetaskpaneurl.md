---
title: External. NavigateTaskPaneURL (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. NavigateTaskPaneURL (método)
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Método NavigateTaskPaneURL de Windows Media Player
- Método NavigateTaskPaneURL de Windows Media Player, clase externa
- Clase externa Windows Media Player, método NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698593"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="33413-107">External. NavigateTaskPaneURL (método)</span><span class="sxs-lookup"><span data-stu-id="33413-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="33413-108">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="33413-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="33413-110">El método **NavigateTaskPaneURL** abre una página web en el panel de tareas especificado y cambia el foco al panel especificado.</span><span class="sxs-lookup"><span data-stu-id="33413-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="33413-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33413-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="33413-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33413-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33413-113">*bstrKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33413-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33413-114">**Cadena** que contiene el nombre de clave de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="33413-115">(necesario)</span><span class="sxs-lookup"><span data-stu-id="33413-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="33413-116">*bstrTaskPane* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33413-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33413-117">**Cadena** que contiene el nombre del panel de tareas en el que se abre la Página Web.</span><span class="sxs-lookup"><span data-stu-id="33413-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="33413-118">(necesario)</span><span class="sxs-lookup"><span data-stu-id="33413-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="33413-119">*bstrParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="33413-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33413-120">**Cadena** que contiene los parámetros de cadena de consulta que se van a anexar a la dirección URL especificada por el elemento **Navigate** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="33413-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="33413-121">(opcional).</span><span class="sxs-lookup"><span data-stu-id="33413-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33413-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33413-122">Return value</span></span>

<span data-ttu-id="33413-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="33413-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33413-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33413-124">Remarks</span></span>

<span data-ttu-id="33413-125">Desplazarse a un panel que la tienda en línea no admite puede hacer que la tienda en línea actual cambie.</span><span class="sxs-lookup"><span data-stu-id="33413-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="33413-126">El valor especificado para *bstrParams* solo es válido cuando se llama a **NavigateTaskPaneURL** desde páginas web proporcionadas por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="33413-127">En la tabla siguiente se muestran los valores válidos para *bstrTaskPane* y el panel de tareas asociado para cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="33413-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="33413-128">Value</span><span class="sxs-lookup"><span data-stu-id="33413-128">Value</span></span>            | <span data-ttu-id="33413-129">Panel de tareas</span><span class="sxs-lookup"><span data-stu-id="33413-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="33413-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="33413-130">**ServiceTask1**</span></span> | <span data-ttu-id="33413-131">Primer panel de tareas de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-131">First online store task pane.</span></span>  |
| <span data-ttu-id="33413-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="33413-132">**ServiceTask2**</span></span> | <span data-ttu-id="33413-133">Segundo panel de tareas de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-133">Second online store task pane.</span></span> |
| <span data-ttu-id="33413-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="33413-134">**ServiceTask3**</span></span> | <span data-ttu-id="33413-135">Tercer panel de tareas de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="33413-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="33413-136">El código de la página web debe especificar un valor para [external. SelectedTaskPane](external-selectedtaskpane.md) al cargar para asegurarse de que se resalta el botón correcto del panel de tareas después de completar la navegación.</span><span class="sxs-lookup"><span data-stu-id="33413-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="33413-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="33413-137">Examples</span></span>

<span data-ttu-id="33413-138">En el ejemplo de código siguiente se muestra cómo **NavigateTaskPaneURL** crea la dirección URL de la página web que se va a mostrar para **ServiceTask1**.</span><span class="sxs-lookup"><span data-stu-id="33413-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="33413-139">Ejemplo del elemento **Navigate** :</span><span class="sxs-lookup"><span data-stu-id="33413-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="33413-140">Llamada de ejemplo al método **NavigateTaskPaneURL** :</span><span class="sxs-lookup"><span data-stu-id="33413-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="33413-141">Ejemplo de dirección URL resultante usada para la página web que se muestra en **ServiceTask1**:</span><span class="sxs-lookup"><span data-stu-id="33413-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="33413-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33413-142">Requirements</span></span>



| <span data-ttu-id="33413-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="33413-143">Requirement</span></span> | <span data-ttu-id="33413-144">Value</span><span class="sxs-lookup"><span data-stu-id="33413-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33413-145">Versión</span><span class="sxs-lookup"><span data-stu-id="33413-145">Version</span></span><br/> | <span data-ttu-id="33413-146">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="33413-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="33413-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33413-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="33413-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33413-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33413-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="33413-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33413-150">**Objeto externo para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="33413-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="33413-151">**External. SelectedTaskPane**</span><span class="sxs-lookup"><span data-stu-id="33413-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





