---
description: El método GetGPRM recupera el registro de parámetros general especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Método GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537887"
---
# <a name="getgprm-method"></a><span data-ttu-id="aef99-103">Método GetGPRM</span><span class="sxs-lookup"><span data-stu-id="aef99-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="aef99-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aef99-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="aef99-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="aef99-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="aef99-106">El `GetGPRM` método recupera el registro de parámetros general especificado.</span><span class="sxs-lookup"><span data-stu-id="aef99-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="aef99-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aef99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef99-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="aef99-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="aef99-109">Especifica el registro que se va a recuperar como un entero.</span><span class="sxs-lookup"><span data-stu-id="aef99-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="aef99-110">El valor debe oscilar entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="aef99-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef99-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aef99-111">Return Value</span></span>

<span data-ttu-id="aef99-112">Devuelve un valor entero que representa el registro especificado.</span><span class="sxs-lookup"><span data-stu-id="aef99-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aef99-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aef99-113">Remarks</span></span>

<span data-ttu-id="aef99-114">Este método no es necesario para ninguna funcionalidad de navegación o reproducción de DVD que use el objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="aef99-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="aef99-115">Se proporciona a los usuarios con un conocimiento exhaustivo de la especificación de DVD que desea implementar características avanzadas.</span><span class="sxs-lookup"><span data-stu-id="aef99-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="aef99-116">GPRMs se puede usar para contener cualquier valor, por lo que se pueden establecer y leer libremente.</span><span class="sxs-lookup"><span data-stu-id="aef99-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="aef99-117">Pero como GPRMs se usan también para almacenar comandos de disco, el cambio de sus valores con [**SetGPRM**](setgprm-method.md) puede producir un comportamiento impredecible.</span><span class="sxs-lookup"><span data-stu-id="aef99-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="aef99-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="aef99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef99-119">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="aef99-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



