---
description: Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559924"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="101b6-103">Materiales (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="101b6-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="101b6-104">Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="101b6-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="101b6-105">Las propiedades de material detallan las características de reflexión difusa, reflexión ambiente, emisión ligera y resaltado especular de un material.</span><span class="sxs-lookup"><span data-stu-id="101b6-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="101b6-106">Direct3D usa la estructura [**D3DMATERIAL9**](d3dmaterial9.md) para incluir toda la información de propiedades de materiales.</span><span class="sxs-lookup"><span data-stu-id="101b6-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="101b6-107">A excepción de la propiedad especular, cada propiedad se describe como un color RGBA que representa la cantidad de las partes rojas, verdes y azules de un determinado tipo de luz reflejada y un factor de mezcla alfa.</span><span class="sxs-lookup"><span data-stu-id="101b6-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="101b6-108">Reflexión difusa y ambiente</span><span class="sxs-lookup"><span data-stu-id="101b6-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="101b6-109">Los miembros difusos y ambiente de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) describen cómo un material refleja el ambiente y la luz difusa en una escena.</span><span class="sxs-lookup"><span data-stu-id="101b6-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="101b6-110">Dado que la mayoría de las escenas contienen mucha más luz difusa que la luz ambiente, la reflexión difusa reproduce la parte más grande al determinar el color.</span><span class="sxs-lookup"><span data-stu-id="101b6-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="101b6-111">Además, dado que la luz difusa es direccional, el ángulo de incidencia de la luz difusa afecta a la intensidad global de la reflexión.</span><span class="sxs-lookup"><span data-stu-id="101b6-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="101b6-112">La reflexión difusa es más grande cuando la luz produce un vértice paralelo a la normal del vértice.</span><span class="sxs-lookup"><span data-stu-id="101b6-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="101b6-113">A medida que aumenta el ángulo, disminuye el efecto del reflejo difuso.</span><span class="sxs-lookup"><span data-stu-id="101b6-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="101b6-114">La cantidad de luz reflejada es el coseno del ángulo entre la luz entrante y la normal del vértice, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="101b6-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![Ilustración de la cantidad de luz reflejada](images/incident.png)

<span data-ttu-id="101b6-116">La reflexión ambiente, como la luz ambiente, no es direccional.</span><span class="sxs-lookup"><span data-stu-id="101b6-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="101b6-117">La reflexión ambiente tiene un impacto menor en el color aparente de un objeto representado, pero afecta al color general y es más apreciable cuando la luz difusa o ninguna luz no refleja el material.</span><span class="sxs-lookup"><span data-stu-id="101b6-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="101b6-118">La reflexión ambiente de un material se ve afectada por el conjunto de luz ambiente de una escena llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con la \_ marca de ambiente D3DRS.</span><span class="sxs-lookup"><span data-stu-id="101b6-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="101b6-119">La reflexión difusa y de ambiente funcionan conjuntamente para determinar el color percibido de un objeto, y suelen ser valores idénticos.</span><span class="sxs-lookup"><span data-stu-id="101b6-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="101b6-120">Por ejemplo, para representar un objeto cristalino azul, cree un material que refleje solo el componente azul de la luz difusa y ambiente.</span><span class="sxs-lookup"><span data-stu-id="101b6-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="101b6-121">Cuando se coloca en una habitación con una luz blanca, el cristal parece azul.</span><span class="sxs-lookup"><span data-stu-id="101b6-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="101b6-122">Sin embargo, en un salón que solo tiene luz roja, el mismo cristal parecería negro, porque su material no refleja la luz roja.</span><span class="sxs-lookup"><span data-stu-id="101b6-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="101b6-123">Emisión</span><span class="sxs-lookup"><span data-stu-id="101b6-123">Emission</span></span>

<span data-ttu-id="101b6-124">Los materiales se pueden usar para hacer que un objeto representado parezca autoluminosa.</span><span class="sxs-lookup"><span data-stu-id="101b6-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="101b6-125">El miembro emisor de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) se usa para describir el color y la transparencia de la luz emitida.</span><span class="sxs-lookup"><span data-stu-id="101b6-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="101b6-126">La emisión afecta al color de un objeto y puede, por ejemplo, hacer un material oscuro más brillante y tomar parte del color emitido.</span><span class="sxs-lookup"><span data-stu-id="101b6-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="101b6-127">Puede usar la propiedad emisor de un material para agregar la ilusión de que un objeto emite luz, sin incurrir en la sobrecarga computacional de agregar una luz a la escena.</span><span class="sxs-lookup"><span data-stu-id="101b6-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="101b6-128">En el caso del cristal azul, la propiedad emisor es útil si desea que aparezca el cristal para que se ilumine, pero no se convierta luz en otros objetos de la escena.</span><span class="sxs-lookup"><span data-stu-id="101b6-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="101b6-129">Recuerde que los materiales con propiedades emisor no emiten luz que se puede reflejar en otros objetos de una escena.</span><span class="sxs-lookup"><span data-stu-id="101b6-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="101b6-130">Para lograr esta luz reflejada, debe colocar una luz adicional dentro de la escena.</span><span class="sxs-lookup"><span data-stu-id="101b6-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="101b6-131">Reflexión especular</span><span class="sxs-lookup"><span data-stu-id="101b6-131">Specular Reflection</span></span>

<span data-ttu-id="101b6-132">La reflexión especular crea resaltados en los objetos, por lo que aparecen de forma brillante.</span><span class="sxs-lookup"><span data-stu-id="101b6-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="101b6-133">La estructura [**D3DMATERIAL9**](d3dmaterial9.md) contiene dos miembros que describen el color de resaltado especular, así como el brillo general del material.</span><span class="sxs-lookup"><span data-stu-id="101b6-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="101b6-134">Para establecer el color de los reflejos especulares, establezca el miembro especular en el color RGBA deseado: los colores más comunes son blanco o gris claro.</span><span class="sxs-lookup"><span data-stu-id="101b6-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="101b6-135">Los valores que se establecen en el control miembro de la potencia controlan la nitidez de los efectos especulares.</span><span class="sxs-lookup"><span data-stu-id="101b6-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="101b6-136">Los reflejos especulares pueden crear efectos drásticos.</span><span class="sxs-lookup"><span data-stu-id="101b6-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="101b6-137">Dibujo de nuevo en la analogía azul de cristal: un valor de potencia mayor crea resaltes especulares más nítidos, lo que parece que el cristal es bastante brillante.</span><span class="sxs-lookup"><span data-stu-id="101b6-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="101b6-138">Los valores más pequeños aumentan el área del efecto, creando una reflexión mate que hace que la apariencia de cristal sea helada.</span><span class="sxs-lookup"><span data-stu-id="101b6-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="101b6-139">Para que un objeto sea realmente mate, establezca el miembro de potencia en cero y el color en especular en negro.</span><span class="sxs-lookup"><span data-stu-id="101b6-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="101b6-140">Experimente con diferentes niveles de reflexión para obtener una apariencia realista para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="101b6-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="101b6-141">En la ilustración siguiente se muestran dos modelos idénticos.</span><span class="sxs-lookup"><span data-stu-id="101b6-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="101b6-142">La parte de la izquierda usa una potencia de reflexión especular de 10; el modelo de la derecha no tiene reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="101b6-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![Ilustración de los modelos de reflexión especular](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="101b6-144">Establecer propiedades de materiales</span><span class="sxs-lookup"><span data-stu-id="101b6-144">Setting Material Properties</span></span>

<span data-ttu-id="101b6-145">Los dispositivos de representación de Direct3D se pueden representar con un conjunto de propiedades de material a la vez.</span><span class="sxs-lookup"><span data-stu-id="101b6-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="101b6-146">En una aplicación de C++, establezca las propiedades de material que el sistema utiliza mediante la preparación de una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y, a continuación, la llamada al método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .</span><span class="sxs-lookup"><span data-stu-id="101b6-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="101b6-147">Para preparar la estructura [**D3DMATERIAL9**](d3dmaterial9.md) para su uso, establezca la información de la propiedad en la estructura para crear el efecto deseado durante la representación.</span><span class="sxs-lookup"><span data-stu-id="101b6-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="101b6-148">En el ejemplo de código siguiente se configura la estructura **D3DMATERIAL9** para un material púrpura con resaltes especulares blancos nítidos.</span><span class="sxs-lookup"><span data-stu-id="101b6-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="101b6-149">Después de preparar la estructura [**D3DMATERIAL9**](d3dmaterial9.md) , aplique las propiedades llamando al método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo de representación.</span><span class="sxs-lookup"><span data-stu-id="101b6-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="101b6-150">Este método acepta la dirección de una estructura **D3DMATERIAL9** preparada como su único parámetro.</span><span class="sxs-lookup"><span data-stu-id="101b6-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="101b6-151">Puede llamar a **IDirect3DDevice9:: SetMaterial** con la nueva información según sea necesario para actualizar las propiedades de material del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="101b6-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="101b6-152">En el ejemplo de código siguiente se muestra cómo podría ser el código.</span><span class="sxs-lookup"><span data-stu-id="101b6-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="101b6-153">Al crear un dispositivo Direct3D, el material actual se establece automáticamente en el valor predeterminado que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="101b6-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="101b6-154">Miembro</span><span class="sxs-lookup"><span data-stu-id="101b6-154">Member</span></span>   | <span data-ttu-id="101b6-155">Valor</span><span class="sxs-lookup"><span data-stu-id="101b6-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="101b6-156">Difusa</span><span class="sxs-lookup"><span data-stu-id="101b6-156">Diffuse</span></span>  | <span data-ttu-id="101b6-157">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="101b6-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="101b6-158">Especular</span><span class="sxs-lookup"><span data-stu-id="101b6-158">Specular</span></span> | <span data-ttu-id="101b6-159">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="101b6-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="101b6-160">Ambiente</span><span class="sxs-lookup"><span data-stu-id="101b6-160">Ambient</span></span>  | <span data-ttu-id="101b6-161">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="101b6-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="101b6-162">Emisor de luz</span><span class="sxs-lookup"><span data-stu-id="101b6-162">Emissive</span></span> | <span data-ttu-id="101b6-163">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="101b6-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="101b6-164">Power</span><span class="sxs-lookup"><span data-stu-id="101b6-164">Power</span></span>    | <span data-ttu-id="101b6-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="101b6-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="101b6-166">Recuperación de propiedades de materiales</span><span class="sxs-lookup"><span data-stu-id="101b6-166">Retrieving Material Properties</span></span>

<span data-ttu-id="101b6-167">Recupera las propiedades de material que el dispositivo de representación está usando actualmente llamando al método [**IDirect3DDevice9:: GetMaterial**](/windows/desktop/api) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="101b6-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="101b6-168">A diferencia del método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9:: GetMaterial** no requiere preparación.</span><span class="sxs-lookup"><span data-stu-id="101b6-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="101b6-169">El método **IDirect3DDevice9:: GetMaterial** acepta la dirección de una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y rellena la estructura proporcionada con información que describe las propiedades del material actual antes de devolver.</span><span class="sxs-lookup"><span data-stu-id="101b6-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="101b6-170">Si la aplicación no especifica propiedades de material para la representación, el sistema utiliza un material predeterminado.</span><span class="sxs-lookup"><span data-stu-id="101b6-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="101b6-171">El material predeterminado refleja todos los colores difusos luminosos, por ejemplo, sin reflexión de ambiente o especular y sin color de emisor.</span><span class="sxs-lookup"><span data-stu-id="101b6-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="101b6-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="101b6-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="101b6-173">Luces y materiales</span><span class="sxs-lookup"><span data-stu-id="101b6-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
