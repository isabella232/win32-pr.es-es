---
title: Redistribuir Windows Media Player 11
description: Redistribuir Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075496"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="ec1ad-103">Redistribuir Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ec1ad-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="ec1ad-104">Puede instalar Windows Media Player 11 en Windows XP con uno de los siguientes programas de instalación, donde *localeId* es un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="ec1ad-105">WMP11-WindowsXP-x86-*localeId*. exe</span><span class="sxs-lookup"><span data-stu-id="ec1ad-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="ec1ad-106">WMP11-WindowsXP-x64-*localeId*. exe</span><span class="sxs-lookup"><span data-stu-id="ec1ad-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="ec1ad-107">Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin solicitud de reinicio o reinicio.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="ec1ad-108">En la tabla siguiente se muestran parámetros adicionales que puede usar con el programa de instalación de Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="ec1ad-109">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ec1ad-109">Parameter</span></span>              | <span data-ttu-id="ec1ad-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec1ad-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1ad-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="ec1ad-111">/NoMigrate</span></span>             | <span data-ttu-id="ec1ad-112">Impedir la migración de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ec1ad-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="ec1ad-113">/NestedRestore</span></span>         | <span data-ttu-id="ec1ad-114">Cree un punto de restauración del sistema anidado.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-114">Create a nested system restore point.</span></span> <span data-ttu-id="ec1ad-115">Úselo si la aplicación crea un punto de restauración del sistema para anidar el punto de restauración de Windows Media Player en el punto de restauración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ec1ad-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="ec1ad-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="ec1ad-117">No permitir la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="ec1ad-118">Esta marca deshabilitará la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="ec1ad-119">En la mayoría de los casos, esta marca no debe usarse para la redistribución de software general.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="ec1ad-120">Esto solo debe usarse cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos de Windows Media Player a una versión anterior del reproductor.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="ec1ad-121">Esta marca solo se debe usar para la instalación corporativa o la instalación del fabricante de equipos originales (OEM).</span><span class="sxs-lookup"><span data-stu-id="ec1ad-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="ec1ad-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="ec1ad-122">/DefaultService</span></span>        | <span data-ttu-id="ec1ad-123">Establezca la tienda en línea inicial.</span><span class="sxs-lookup"><span data-stu-id="ec1ad-123">Set the initial online store.</span></span> <span data-ttu-id="ec1ad-124">Para obtener más información, consulte [configuración de parámetros de línea de comandos para tiendas en línea](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="ec1ad-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ec1ad-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec1ad-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec1ad-126">**Redistribuir el software de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="ec1ad-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




