---
description: La propiedad DVDAdm. DisableScreenSaver activa o desactiva el protector de pantalla del sistema.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propiedad DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906361"
---
# <a name="disablescreensaver-property"></a><span data-ttu-id="67597-103">Propiedad DisableScreenSaver</span><span class="sxs-lookup"><span data-stu-id="67597-103">DisableScreenSaver Property</span></span>

> [!Note]  
> <span data-ttu-id="67597-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67597-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="67597-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="67597-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="67597-106">La `DVDAdm.DisableScreenSaver` propiedad activa o desactiva el protector de pantalla del sistema.</span><span class="sxs-lookup"><span data-stu-id="67597-106">The `DVDAdm.DisableScreenSaver` property turns the system screen saver on or off.</span></span>

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a><span data-ttu-id="67597-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67597-107">Return Value</span></span>

<span data-ttu-id="67597-108">Devuelve un valor booleano que indica si la configuración del protector de pantalla del sistema está deshabilitada para la aplicación de reproducción de DVD; True significa que la configuración está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="67597-108">Returns a Boolean value indicating whether the system's screen saver settings are disabled for the DVD player application; true means the settings are disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="67597-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67597-109">Remarks</span></span>

<span data-ttu-id="67597-110">Esta propiedad es de lectura/escritura y su valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="67597-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="67597-111">Al ver un disco DVD-Video, un usuario no suele usar el mouse o el teclado durante largos períodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="67597-111">When viewing a DVD-Video disc, a user typically does not use the mouse or keyboard for extended periods of time.</span></span> <span data-ttu-id="67597-112">Por lo tanto, el control MSWebDVD de ActiveX® deshabilita el protector de pantalla del sistema de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="67597-112">The MSWebDVD ActiveX® control therefore disables the system screen saver by default.</span></span> <span data-ttu-id="67597-113">Object</span><span class="sxs-lookup"><span data-stu-id="67597-113">Object</span></span>

## <a name="see-also"></a><span data-ttu-id="67597-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="67597-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67597-115">**RestoreScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="67597-115">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)
</dt> <dt>

[<span data-ttu-id="67597-116">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="67597-116">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



