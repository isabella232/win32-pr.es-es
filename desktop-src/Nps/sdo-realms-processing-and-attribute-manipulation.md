---
title: Procesamiento de dominios y manipulación de atributos
description: El procesamiento de los territorios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita el acceso.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792574"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="85f2e-103">Procesamiento de dominios y manipulación de atributos</span><span class="sxs-lookup"><span data-stu-id="85f2e-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="85f2e-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="85f2e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="85f2e-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="85f2e-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="85f2e-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="85f2e-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="85f2e-107">El procesamiento de los territorios, que también se conoce como manipulación de atributos, hace referencia a la transformación del nombre del usuario que solicita el acceso.</span><span class="sxs-lookup"><span data-stu-id="85f2e-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="85f2e-108">También se puede manipular el identificador de la estación de llamada y el identificador de estación llamada.</span><span class="sxs-lookup"><span data-stu-id="85f2e-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="85f2e-109">Las reglas de procesamiento de dominios forman parte de la colección de atributos de Perfil de proxy.</span><span class="sxs-lookup"><span data-stu-id="85f2e-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="85f2e-110">Para cada manipulación, debe crear dos atributos [de regla de manipulación](/windows/desktop/Nps/sdo-manipulation-rule) .</span><span class="sxs-lookup"><span data-stu-id="85f2e-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="85f2e-111">Cada uno de estos atributos es un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="85f2e-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="85f2e-112">La primera regla contiene una expresión regular que representa el patrón que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="85f2e-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="85f2e-113">La segunda regla contiene una expresión regular que representa el texto de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="85f2e-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="85f2e-114">También debe crear un atributo [de destino de manipulación](/windows/desktop/Nps/sdo-manipulation-target) .</span><span class="sxs-lookup"><span data-stu-id="85f2e-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="85f2e-115">Este atributo es una enumeración que especifica qué parte de la información del usuario se va a manipular.</span><span class="sxs-lookup"><span data-stu-id="85f2e-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="85f2e-116">Es importante el orden en el que se crean los atributos.</span><span class="sxs-lookup"><span data-stu-id="85f2e-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="85f2e-117">NPS procesa los atributos en el orden en que se crearon.</span><span class="sxs-lookup"><span data-stu-id="85f2e-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="85f2e-118">En la tabla siguiente se muestra un ejemplo de un conjunto de atributos de manipulación.</span><span class="sxs-lookup"><span data-stu-id="85f2e-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="85f2e-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="85f2e-119">Name</span></span>                 | <span data-ttu-id="85f2e-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="85f2e-120">Type</span></span>         | <span data-ttu-id="85f2e-121">Valor de cadena</span><span class="sxs-lookup"><span data-stu-id="85f2e-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="85f2e-122">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="85f2e-122">msManipulationRule</span></span>   | <span data-ttu-id="85f2e-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="85f2e-123">**VT\_BSTR**</span></span> | <span data-ttu-id="85f2e-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="85f2e-124">"@company.com"</span></span>   |
| <span data-ttu-id="85f2e-125">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="85f2e-125">msManipulationRule</span></span>   | <span data-ttu-id="85f2e-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="85f2e-126">**VT\_BSTR**</span></span> | <span data-ttu-id="85f2e-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="85f2e-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="85f2e-128">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="85f2e-128">msManipulationRule</span></span>   | <span data-ttu-id="85f2e-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="85f2e-129">**VT\_BSTR**</span></span> | <span data-ttu-id="85f2e-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="85f2e-130">"^.+@"</span></span>           |
| <span data-ttu-id="85f2e-131">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="85f2e-131">msManipulationRule</span></span>   | <span data-ttu-id="85f2e-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="85f2e-132">**VT\_BSTR**</span></span> | <span data-ttu-id="85f2e-133">"guest@"</span><span class="sxs-lookup"><span data-stu-id="85f2e-133">"guest@"</span></span>         |
| <span data-ttu-id="85f2e-134">msManipulationTarget</span><span class="sxs-lookup"><span data-stu-id="85f2e-134">msManipulationTarget</span></span> | <span data-ttu-id="85f2e-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="85f2e-135">**VT\_I4**</span></span>   | <span data-ttu-id="85f2e-136">"1"</span><span class="sxs-lookup"><span data-stu-id="85f2e-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="85f2e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85f2e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85f2e-138">Jerarquía del modelo de objetos</span><span class="sxs-lookup"><span data-stu-id="85f2e-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="85f2e-139">Atributos compatibles con SDO</span><span class="sxs-lookup"><span data-stu-id="85f2e-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="85f2e-140">Creación de una directiva de solicitud de conexión</span><span class="sxs-lookup"><span data-stu-id="85f2e-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="85f2e-141">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="85f2e-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="85f2e-142">**ISdoDictionaryOld**</span><span class="sxs-lookup"><span data-stu-id="85f2e-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="85f2e-143">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="85f2e-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 