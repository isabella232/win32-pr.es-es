---
title: Show (método)
description: Show (método)
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704938"
---
# <a name="show-method"></a><span data-ttu-id="8d23c-103">Show (método)</span><span class="sxs-lookup"><span data-stu-id="8d23c-103">Show Method</span></span>

<span data-ttu-id="8d23c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8d23c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8d23c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="8d23c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8d23c-106">Hace que el carácter especificado sea visible y reproduzca la animación **mostrada** asociada.</span><span class="sxs-lookup"><span data-stu-id="8d23c-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="8d23c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="8d23c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8d23c-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Mostrar* \*  \[ *rápido*\]</span><span class="sxs-lookup"><span data-stu-id="8d23c-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="8d23c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8d23c-109">Part</span></span>   | <span data-ttu-id="8d23c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d23c-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d23c-111">*Rápido*</span><span class="sxs-lookup"><span data-stu-id="8d23c-111">*Fast*</span></span> | <span data-ttu-id="8d23c-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8d23c-112">Optional.</span></span> <span data-ttu-id="8d23c-113">Una expresión booleana que especifica si el servidor reproduce la animación **que se muestra** .</span><span class="sxs-lookup"><span data-stu-id="8d23c-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="8d23c-114">**True** Omite la animación de estado **que se muestra** .</span><span class="sxs-lookup"><span data-stu-id="8d23c-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="8d23c-115">**False** (valor predeterminado) no omite la animación de estado **que se muestra** .</span><span class="sxs-lookup"><span data-stu-id="8d23c-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d23c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d23c-116">Remarks</span></span>

<span data-ttu-id="8d23c-117">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="8d23c-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="8d23c-118">Además, si la animación **que se muestra** asociada no se ha cargado y no se ha especificado el parámetro **Fast** como **true**, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con un número de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="8d23c-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="8d23c-119">Por lo tanto, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación de estado **que se muestra** antes de llamar al método **Show** .</span><span class="sxs-lookup"><span data-stu-id="8d23c-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="8d23c-120">Evite establecer el parámetro **Fast** en **true** sin reproducir primero una animación de antemano; de lo contrario, el marco de caracteres puede mostrarse sin ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="8d23c-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="8d23c-121">En concreto, tenga en cuenta que si llama a [**moveTo**](moveto-method.md) cuando el carácter no está visible, no se reproduce ninguna animación.</span><span class="sxs-lookup"><span data-stu-id="8d23c-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="8d23c-122">Por lo tanto, si llama al método **Show** con **Fast** establecido en **true**, no se mostrará ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="8d23c-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="8d23c-123">Del mismo modo, si llama a [**Hide**](hide-method.md) y **Show** con **Fast** set en **true**, no habrá ninguna imagen visible.</span><span class="sxs-lookup"><span data-stu-id="8d23c-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d23c-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8d23c-124">See Also</span></span>

[<span data-ttu-id="8d23c-125">**Hide (método)**</span><span class="sxs-lookup"><span data-stu-id="8d23c-125">**Hide method**</span></span>](hide-method.md)


 

