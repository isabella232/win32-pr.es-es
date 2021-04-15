---
description: El método DVDAdm. GetParentalLevel recupera el nivel parental que se guardó por última vez en el registro.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Método GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422766"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="bd0e3-103">Método GetParentalLevel</span><span class="sxs-lookup"><span data-stu-id="bd0e3-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="bd0e3-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bd0e3-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bd0e3-106">El `DVDAdm.GetParentalLevel` método recupera el nivel parental que se guardó por última vez en el registro.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="bd0e3-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd0e3-107">Return Value</span></span>

<span data-ttu-id="bd0e3-108">Devuelve un entero del 1 al 8 que indica el nivel parental predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0e3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd0e3-109">Remarks</span></span>

<span data-ttu-id="bd0e3-110">El nivel parental que recupera este método no es necesariamente el mismo nivel almacenado actualmente en el control MSWebDVD. para obtener el nivel almacenado actualmente en el control, llame al método [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) .</span><span class="sxs-lookup"><span data-stu-id="bd0e3-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="bd0e3-111">Un valor de-1 indica que la administración parental está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="bd0e3-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd0e3-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd0e3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0e3-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="bd0e3-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



