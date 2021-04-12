---
description: La propiedad DVDAdm. DefaultMenuLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para los menús.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propiedad DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152554"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="772e2-103">Propiedad DefaultMenuLCID</span><span class="sxs-lookup"><span data-stu-id="772e2-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="772e2-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="772e2-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="772e2-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="772e2-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="772e2-106">La `DVDAdm.DefaultMenuLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para los menús.</span><span class="sxs-lookup"><span data-stu-id="772e2-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="772e2-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="772e2-107">Return Value</span></span>

<span data-ttu-id="772e2-108">Devuelve un valor entero que representa el LCID tal y como se almacena en la configuración del registro de la aplicación de DVD.</span><span class="sxs-lookup"><span data-stu-id="772e2-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="772e2-109">Este valor no es necesariamente el mismo que el idioma del menú predeterminado que se creó en el DVD.</span><span class="sxs-lookup"><span data-stu-id="772e2-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="772e2-110">Para ver el intervalo de LCID válidos, consulte la documentación de Win32 en el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="772e2-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="772e2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="772e2-111">Remarks</span></span>

<span data-ttu-id="772e2-112">Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="772e2-112">This property is read/write with no default value.</span></span> <span data-ttu-id="772e2-113">Si no se especifica ningún LCID de menú predeterminado, el objeto MSDVDAdm usará el idioma que esté marcado como idioma predeterminado en el disco.</span><span class="sxs-lookup"><span data-stu-id="772e2-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="772e2-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="772e2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772e2-115">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="772e2-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



