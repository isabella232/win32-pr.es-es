---
description: El método DVDAdm. RestoreScreenSaver restaura la configuración del protector de pantalla del sistema.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Método RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677098"
---
# <a name="restorescreensaver-method"></a><span data-ttu-id="47875-103">Método RestoreScreenSaver</span><span class="sxs-lookup"><span data-stu-id="47875-103">RestoreScreenSaver Method</span></span>

> [!Note]  
> <span data-ttu-id="47875-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="47875-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="47875-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="47875-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="47875-106">El `DVDAdm.RestoreScreenSaver` método restaura la configuración del protector de pantalla del sistema.</span><span class="sxs-lookup"><span data-stu-id="47875-106">The `DVDAdm.RestoreScreenSaver` method restores the system screen saver settings.</span></span>

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a><span data-ttu-id="47875-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47875-107">Return Value</span></span>

<span data-ttu-id="47875-108">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="47875-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47875-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47875-109">Remarks</span></span>

<span data-ttu-id="47875-110">Por lo general, una aplicación de DVD deshabilitará el protector de pantalla del sistema al iniciarse si se establece la propiedad [**DisableScreenSaver**](disablescreensaver-property.md) en true y, a continuación, se vuelve a habilitar el protector de pantalla cuando se cierra la aplicación de DVD mediante una llamada a `RestoreScreenSaver` .</span><span class="sxs-lookup"><span data-stu-id="47875-110">Generally, a DVD application will disable the system's screen saver on startup by setting the [**DisableScreenSaver**](disablescreensaver-property.md) property to true, and then re-enable the screen saver again when the DVD application is closed by calling `RestoreScreenSaver`.</span></span> <span data-ttu-id="47875-111">Si una aplicación no usa la configuración del protector de pantalla del sistema, no tiene que llamar a este método o establecer la propiedad **DisableScreenSaver** .</span><span class="sxs-lookup"><span data-stu-id="47875-111">If an application does not use the system's screen saver settings, it does not have to call this method or set the **DisableScreenSaver** property.</span></span>

## <a name="see-also"></a><span data-ttu-id="47875-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="47875-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47875-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="47875-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



