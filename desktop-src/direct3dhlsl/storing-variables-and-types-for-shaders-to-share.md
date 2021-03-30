---
title: Almacenar variables y tipos para los sombreadores que se van a compartir
description: El objeto de vinculación de clases es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984071"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="4704c-103">Almacenar variables y tipos para los sombreadores que se van a compartir</span><span class="sxs-lookup"><span data-stu-id="4704c-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="4704c-104">El objeto de vinculación de clases es un espacio de nombres para variables y tipos que pueden compartir varios sombreadores.</span><span class="sxs-lookup"><span data-stu-id="4704c-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="4704c-105">Cuando se pasa un objeto de vinculación de clase en una llamada a para crear un sombreador, el tiempo de ejecución recopila una lista de variables y tipos que pueden implementar cada interfaz en el sombreador y almacena los nombres de esas variables y tipos en el objeto de vinculación de clases.</span><span class="sxs-lookup"><span data-stu-id="4704c-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="4704c-106">Por lo tanto, cuando se llama al método [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para generar instancias de clase desde el objeto de vinculación de clase, el runtime puede recuperar la variable o el tipo que se corresponde con el nombre proporcionado en cada sombreador (si ese nombre es válido para un sombreador determinado) y que se crea con el objeto de vinculación de clase especificado.</span><span class="sxs-lookup"><span data-stu-id="4704c-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="4704c-107">Por ejemplo, supongamos que tiene una clase **Light** que implementa una interfaz de **color** y usa esta clase en el sombreador de vértices y en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4704c-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="4704c-108">Al crear un sombreador (por ejemplo, llamando a [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), el tiempo de ejecución determina que el tipo de clase **Light** está disponible en los sombreadores de vértices y píxeles y agrega el tipo de clase **Light** al objeto de vinculación de clase.</span><span class="sxs-lookup"><span data-stu-id="4704c-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="4704c-109">Después, puede crear una instancia de **Light** en la ubicación que desee, enlazar los recursos de ambos sombreadores y pasar esta instancia en la matriz de instancias de clase al establecer el sombreador en el dispositivo (por ejemplo, mediante una llamada a [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="4704c-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="4704c-110">A continuación, el tiempo de ejecución realiza la siguiente secuencia:</span><span class="sxs-lookup"><span data-stu-id="4704c-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="4704c-111">Comprueba que la instancia de se creó con el mismo objeto de vinculación de clase.</span><span class="sxs-lookup"><span data-stu-id="4704c-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="4704c-112">Comprueba que el tipo de clase **Light** está disponible en los sombreadores de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="4704c-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="4704c-113">Selecciona las tablas de funciones correctas, que pueden ser diferentes para los sombreadores de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="4704c-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="4704c-114">Envía los desplazamientos que proporciona la instancia de.</span><span class="sxs-lookup"><span data-stu-id="4704c-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="4704c-115">En última instancia, el objeto de vinculación de clases es un repositorio de nombres de tipo y variable.</span><span class="sxs-lookup"><span data-stu-id="4704c-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="4704c-116">El número máximo de nombres disponibles para cada elemento (tipo y variable) es de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="4704c-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="4704c-117">Cuanto más largas sean los nombres de tipo y variable, mayor será el requisito de almacenamiento de los metadatos de la interfaz que se almacenan por cada sombreador.</span><span class="sxs-lookup"><span data-stu-id="4704c-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="4704c-118">Esto se debe a que el Runtime debe almacenar una asignación para estos nombres para cada sombreador.</span><span class="sxs-lookup"><span data-stu-id="4704c-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4704c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4704c-119">Related Topics</span></span>

[<span data-ttu-id="4704c-120">Vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="4704c-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="4704c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4704c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4704c-122">Vinculación dinámica</span><span class="sxs-lookup"><span data-stu-id="4704c-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 