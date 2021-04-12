---
title: Propiedad RaiseRequestErrors
description: Propiedad RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271204"
---
# <a name="raiserequesterrors-property"></a><span data-ttu-id="caf98-103">Propiedad RaiseRequestErrors</span><span class="sxs-lookup"><span data-stu-id="caf98-103">RaiseRequestErrors Property</span></span>

<span data-ttu-id="caf98-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="caf98-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="caf98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="caf98-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-106">Devuelve o establece si se producen errores en las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="caf98-106">Returns or sets whether errors for requests are raised.</span></span>

</dd> <dt>

<span data-ttu-id="caf98-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="caf98-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="caf98-108">\*agente \* \* *. RaiseRequestErrors* \*  \[  =  *booleano*\]</span><span class="sxs-lookup"><span data-stu-id="caf98-108">*agent\*\*\*.RaiseRequestErrors*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="caf98-109">Parte</span><span class="sxs-lookup"><span data-stu-id="caf98-109">Part</span></span>      | <span data-ttu-id="caf98-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="caf98-110">Description</span></span>                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf98-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="caf98-111">*boolean*</span></span> | <span data-ttu-id="caf98-112">Valor booleano que determina si se producen errores en las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="caf98-112">A Boolean value that determines whether errors in requests are raised.</span></span><br/> <span data-ttu-id="caf98-113">Se generan errores de solicitud **true** (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="caf98-113">**True**    (Default) Request errors are raised.</span></span> <br/> <span data-ttu-id="caf98-114">**False**     No se generan errores de solicitud.</span><span class="sxs-lookup"><span data-stu-id="caf98-114">**False**     Request errors are not raised.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caf98-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="caf98-115">Remarks</span></span>

<span data-ttu-id="caf98-116">Esta propiedad le permite determinar si el servidor genera errores que se producen con métodos que admiten objetos de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="caf98-116">This property enables you to determine whether the server raises errors that occur with methods that support [**Request**](/windows/desktop/lwef/the-request-object) objects.</span></span> <span data-ttu-id="caf98-117">Por ejemplo, si especifica un nombre de animación que no existe en un método [**Play**](play-method.md), el servidor genera un error (mostrando el mensaje de error) a menos que establezca esta propiedad en **false**.</span><span class="sxs-lookup"><span data-stu-id="caf98-117">For example, if you specify an animation name that does not exist in a [**Play**](play-method.md)method, the server raises an error (displaying the error message) unless you set this property to **False**.</span></span>

<span data-ttu-id="caf98-118">Puede ser útil para los lenguajes de programación que no proporcionan recuperación cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="caf98-118">It may be useful for programming languages that do not provide recovery when an error is raised.</span></span> <span data-ttu-id="caf98-119">Sin embargo, tenga cuidado al establecer esta propiedad en **false**, ya que podría ser más difícil encontrar errores en el código.</span><span class="sxs-lookup"><span data-stu-id="caf98-119">However, use care when setting this property to **False**, because it might be harder to find errors in your code.</span></span>

 

