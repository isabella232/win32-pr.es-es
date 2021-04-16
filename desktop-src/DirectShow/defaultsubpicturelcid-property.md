---
description: La propiedad DVDAdm. DefaultSubpictureLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de subimagen.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propiedad DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538241"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="78318-103">Propiedad DefaultSubpictureLCID</span><span class="sxs-lookup"><span data-stu-id="78318-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="78318-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78318-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78318-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="78318-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78318-106">La `DVDAdm.DefaultSubpictureLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de subimagen.</span><span class="sxs-lookup"><span data-stu-id="78318-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="78318-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78318-107">Return Value</span></span>

<span data-ttu-id="78318-108">Devuelve un valor entero que representa el LCID de la subimagen predeterminada especificada por el usuario, tal y como se almacena en la configuración del registro de la aplicación de DVD.</span><span class="sxs-lookup"><span data-stu-id="78318-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="78318-109">Este valor no es necesariamente el mismo que el flujo de la subimagen predeterminada que se creó en el DVD.</span><span class="sxs-lookup"><span data-stu-id="78318-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="78318-110">Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="78318-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="78318-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78318-111">Remarks</span></span>

<span data-ttu-id="78318-112">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="78318-112">This property is read/write with no default value.</span></span> <span data-ttu-id="78318-113">Si no se especifica ningún LCID de subimagen predeterminado, el objeto MSDVDAdm reproducirá el flujo de subimagen que está marcado como la secuencia predeterminada en el disco.</span><span class="sxs-lookup"><span data-stu-id="78318-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="78318-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="78318-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78318-115">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="78318-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



