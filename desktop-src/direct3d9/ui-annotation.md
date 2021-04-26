---
description: Use esta anotación para asociar un parámetro de efecto a un control de interfaz de usuario en el entorno host. Esto permitirá a un usuario controlar interactivamente un parámetro de efecto a través de la aplicación host.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Anotación de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef6af352b7dea25df34ce8a5712ad30143d6426
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998592"
---
# <a name="ui-annotation"></a><span data-ttu-id="1d93a-104">Anotación de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="1d93a-104">UI Annotation</span></span>

<span data-ttu-id="1d93a-105">Use esta anotación para asociar un parámetro de efecto a un control de interfaz de usuario en el entorno host.</span><span class="sxs-lookup"><span data-stu-id="1d93a-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="1d93a-106">Esto permitirá a un usuario controlar interactivamente un parámetro de efecto a través de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="1d93a-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="1d93a-107">DXSAS define un conjunto de controles estándar en términos del modelo de datos y el comportamiento básico que los autores pueden esperar de las aplicaciones host.</span><span class="sxs-lookup"><span data-stu-id="1d93a-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="1d93a-108">La anotación de control se usa de la siguiente forma:</span><span class="sxs-lookup"><span data-stu-id="1d93a-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="1d93a-109">where</span><span class="sxs-lookup"><span data-stu-id="1d93a-109">where</span></span>


```
ControlType
```



<span data-ttu-id="1d93a-110">es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="1d93a-110">is one of the following:</span></span>



| <span data-ttu-id="1d93a-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="1d93a-111">ControlType</span></span> | <span data-ttu-id="1d93a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d93a-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="1d93a-113">Tipo de datos interno</span><span class="sxs-lookup"><span data-stu-id="1d93a-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="1d93a-114">Anotaciones de propiedades de control</span><span class="sxs-lookup"><span data-stu-id="1d93a-114">Control Property Annotations</span></span>                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d93a-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1d93a-115">None</span></span>        | <span data-ttu-id="1d93a-116">No se debe mostrar ningún control.</span><span class="sxs-lookup"><span data-stu-id="1d93a-116">No control should be shown.</span></span> <span data-ttu-id="1d93a-117">Tenga en cuenta que un control está visible [si SasUiVisible](#sasuivisible) es True y el tipo de control es cualquier tipo distinto de None.</span><span class="sxs-lookup"><span data-stu-id="1d93a-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="1d93a-118">N/D</span><span class="sxs-lookup"><span data-stu-id="1d93a-118">n/a</span></span>                                                                                                | <span data-ttu-id="1d93a-119">N/D</span><span class="sxs-lookup"><span data-stu-id="1d93a-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="1d93a-120">Any</span><span class="sxs-lookup"><span data-stu-id="1d93a-120">Any</span></span>         | <span data-ttu-id="1d93a-121">Esto implica que no se solicita ningún control especial.</span><span class="sxs-lookup"><span data-stu-id="1d93a-121">This implies that no special control is requested.</span></span> <span data-ttu-id="1d93a-122">El control presentado es el resultado del comportamiento definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d93a-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="1d93a-123">N/D</span><span class="sxs-lookup"><span data-stu-id="1d93a-123">n/a</span></span>                                                                                                | <span data-ttu-id="1d93a-124">N/D</span><span class="sxs-lookup"><span data-stu-id="1d93a-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="1d93a-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="1d93a-125">ColorPicker</span></span> | <span data-ttu-id="1d93a-126">Representar un valor de color como una muestra de color.</span><span class="sxs-lookup"><span data-stu-id="1d93a-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="1d93a-127">El valor se empaqueta en los componentes XYZ del vector asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="1d93a-128">El componente W del vector asociado siempre se establece en uno.</span><span class="sxs-lookup"><span data-stu-id="1d93a-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="1d93a-129">float *N,* *donde N* es de 1 a 4 inclusive.</span><span class="sxs-lookup"><span data-stu-id="1d93a-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="1d93a-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="1d93a-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="1d93a-131">Dirección</span><span class="sxs-lookup"><span data-stu-id="1d93a-131">Direction</span></span>   | <span data-ttu-id="1d93a-132">Vector de dirección.</span><span class="sxs-lookup"><span data-stu-id="1d93a-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="1d93a-133">float *N,* *donde N* es de 2 a 4 inclusive.</span><span class="sxs-lookup"><span data-stu-id="1d93a-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="1d93a-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1d93a-134">None</span></span>                                                                                                         |
| <span data-ttu-id="1d93a-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="1d93a-135">FilePicker</span></span>  | <span data-ttu-id="1d93a-136">Cuadro de diálogo que permite al usuario examinar y seleccionar un archivo.</span><span class="sxs-lookup"><span data-stu-id="1d93a-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="1d93a-137">string</span><span class="sxs-lookup"><span data-stu-id="1d93a-137">string</span></span>                                                                                             | <span data-ttu-id="1d93a-138">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1d93a-138">None</span></span>                                                                                                         |
| <span data-ttu-id="1d93a-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="1d93a-139">ListPicker</span></span>  | <span data-ttu-id="1d93a-140">Lista de valores de cadena desde los que el usuario puede seleccionar una entrada.</span><span class="sxs-lookup"><span data-stu-id="1d93a-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="1d93a-141">Los valores se generan a partir de la [anotación SasUiEnum.](#sasuienum)</span><span class="sxs-lookup"><span data-stu-id="1d93a-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="1d93a-142">Matriz de cadenas junto con un valor entero que contiene el índice del valor de cadena seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="1d93a-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="1d93a-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="1d93a-144">Numérico</span><span class="sxs-lookup"><span data-stu-id="1d93a-144">Numeric</span></span>     | <span data-ttu-id="1d93a-145">Un conjunto de controles de entrada numéricos (por ejemplo, cuadros de texto).</span><span class="sxs-lookup"><span data-stu-id="1d93a-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="1d93a-146">float *M* x *N,* *donde M* y *N* son de 1 a 4 inclusive.</span><span class="sxs-lookup"><span data-stu-id="1d93a-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="1d93a-147">[SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="1d93a-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="1d93a-148">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="1d93a-148">Slider</span></span>      | <span data-ttu-id="1d93a-149">Un conjunto de controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="1d93a-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="1d93a-150">float *M* x *N* donde *M* y *N* son de 1 a 4 inclusive</span><span class="sxs-lookup"><span data-stu-id="1d93a-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="1d93a-151">[SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiSteps,](#sasuisteps) [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="1d93a-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="1d93a-152">String</span><span class="sxs-lookup"><span data-stu-id="1d93a-152">String</span></span>      | <span data-ttu-id="1d93a-153">Cuadro de texto para editar contenido de cadena.</span><span class="sxs-lookup"><span data-stu-id="1d93a-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="1d93a-154">string</span><span class="sxs-lookup"><span data-stu-id="1d93a-154">string</span></span>                                                                                             | <span data-ttu-id="1d93a-155">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1d93a-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="1d93a-156">Si el tipo de datos interno no es idéntico al tipo del parámetro asociado, la conversión se producirá cuando se transfieran datos del parámetro de aplicación host al parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="1d93a-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="1d93a-157">El valor predeterminado es la cadena "None".</span><span class="sxs-lookup"><span data-stu-id="1d93a-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="1d93a-158">Propiedades comunes de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="1d93a-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="1d93a-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="1d93a-159">SasUiDescription</span></span>

<span data-ttu-id="1d93a-160">Use esta anotación para especificar una cadena para describir una herramienta.</span><span class="sxs-lookup"><span data-stu-id="1d93a-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="1d93a-161">Esto se puede usar para elementos de la interfaz de usuario, como sugerencias de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1d93a-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="1d93a-162">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1d93a-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="1d93a-163">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1d93a-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="1d93a-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="1d93a-164">SasUiLabel</span></span>

<span data-ttu-id="1d93a-165">Use esta anotación para especificar una cadena para etiquetar cualquier control de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1d93a-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="1d93a-166">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1d93a-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="1d93a-167">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1d93a-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="1d93a-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="1d93a-168">SasUiVisible</span></span>

<span data-ttu-id="1d93a-169">Use esta anotación para especificar si el parámetro asociado debe mostrarse al usuario.</span><span class="sxs-lookup"><span data-stu-id="1d93a-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="1d93a-170">Si se establece en True, la aplicación host debe mostrar un control de interfaz de usuario para editar el parámetro de efecto anotado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="1d93a-171">Si es false, no se muestra ninguna interfaz de usuario en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="1d93a-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="1d93a-172">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1d93a-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="1d93a-173">El valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="1d93a-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="1d93a-174">Propiedades del control de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="1d93a-174">UI Control Properties</span></span>

<span data-ttu-id="1d93a-175">Las anotaciones de propiedades de control son modificadores adicionales que ayudan a determinar cómo funciona un control determinado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="1d93a-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="1d93a-176">SasUiEnum</span></span>

<span data-ttu-id="1d93a-177">Esta anotación permite restringir el intervalo de valores de un control.</span><span class="sxs-lookup"><span data-stu-id="1d93a-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="1d93a-178">La anotación contiene una cadena de valores delimitados por comas.</span><span class="sxs-lookup"><span data-stu-id="1d93a-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="1d93a-179">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1d93a-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="1d93a-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="1d93a-180">SasUiMax</span></span>

<span data-ttu-id="1d93a-181">Esta anotación especifica el valor máximo del parámetro asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="1d93a-182">Solo se puede asociar a un parámetro con tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="1d93a-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="1d93a-183">El valor máximo del parámetro se calculará realmente como:</span><span class="sxs-lookup"><span data-stu-id="1d93a-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="1d93a-184">PARAMETER \_ TYPE MAX es el valor máximo para el tipo utilizado por el parámetro \_ asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="1d93a-185">Esto significa que el valor del parámetro, teniendo en cuenta la anotación [SasUiMax,](#sasuimax) se calcula como:</span><span class="sxs-lookup"><span data-stu-id="1d93a-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="1d93a-186">El valor predeterminado es FLT \_ MAX tal como se define en Math.h.</span><span class="sxs-lookup"><span data-stu-id="1d93a-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="1d93a-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="1d93a-187">SasUiMin</span></span>

<span data-ttu-id="1d93a-188">Esta anotación especifica el valor mínimo del parámetro asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="1d93a-189">Solo se puede asociar a cualquier parámetro con tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="1d93a-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="1d93a-190">El valor mínimo del parámetro se calculará realmente como:</span><span class="sxs-lookup"><span data-stu-id="1d93a-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="1d93a-191">PARAMETER \_ TYPE MIN es el valor mínimo para el tipo utilizado por el parámetro \_ asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="1d93a-192">Esto significa que el valor del parámetro , teniendo en cuenta la anotación [SasUiMin](#sasuimin) se calcula como:</span><span class="sxs-lookup"><span data-stu-id="1d93a-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="1d93a-193">El valor predeterminado es -FLT \_ MAX, tal como se define en Math.h.</span><span class="sxs-lookup"><span data-stu-id="1d93a-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="1d93a-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="1d93a-194">SasUiSteps</span></span>

<span data-ttu-id="1d93a-195">Esta anotación especifica el número de pasos que se pueden usar al incrementar o disminuir el valor del parámetro asociado.</span><span class="sxs-lookup"><span data-stu-id="1d93a-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="1d93a-196">La anotación solo es significativa en un parámetro con tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="1d93a-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="1d93a-197">Cero especifica que la aplicación host elegirá un número razonable de pasos.</span><span class="sxs-lookup"><span data-stu-id="1d93a-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="1d93a-198">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="1d93a-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="1d93a-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="1d93a-199">SasUiStepsPower</span></span>

<span data-ttu-id="1d93a-200">Esta anotación especifica el exponente en la función de energía, que tiene el intervalo \[ 0,0f, 1,0f \] .</span><span class="sxs-lookup"><span data-stu-id="1d93a-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="1d93a-201">Las aplicaciones host deben implementar el método siguiente al calcular los valores de parámetro:</span><span class="sxs-lookup"><span data-stu-id="1d93a-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="1d93a-202">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="1d93a-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="1d93a-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="1d93a-203">SasUiStride</span></span>

<span data-ttu-id="1d93a-204">Esta anotación especifica el incremento que se debe usar al incrementar o disminuir este valor.</span><span class="sxs-lookup"><span data-stu-id="1d93a-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="1d93a-205">A diferencia de [SasUiSteps,](#sasuisteps) [SasUiStride](#sasuistride) es útil con un control de número, por ejemplo, donde los datos están sin enlazar y el usuario prefiere incrementar el valor del parámetro por pasos en lugar de por un número predefinido de pasos.</span><span class="sxs-lookup"><span data-stu-id="1d93a-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="1d93a-206">Las aplicaciones host deben incrementar (o disminuir en función del comportamiento del control) el valor de SasUiStride como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="1d93a-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="1d93a-207">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="1d93a-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d93a-208">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d93a-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d93a-209">Referencia de anotaciones y semánticas estándar de DirectX</span><span class="sxs-lookup"><span data-stu-id="1d93a-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



