---
title: Redistribuir Windows Media Player 10
description: Redistribuir Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773446"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="881c0-103">Redistribuir Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="881c0-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="881c0-104">Puede instalar Windows Media Player 10 en Windows XP mediante el siguiente programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="881c0-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="881c0-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="881c0-105">MP10Setup.exe</span></span>

<span data-ttu-id="881c0-106">Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin solicitud de reinicio o reinicio.</span><span class="sxs-lookup"><span data-stu-id="881c0-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="881c0-107">En la tabla siguiente se muestran parámetros adicionales que puede usar con el programa de instalación de Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="881c0-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="881c0-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="881c0-108">Parameter</span></span>              | <span data-ttu-id="881c0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="881c0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881c0-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="881c0-110">/NoMigrate</span></span>             | <span data-ttu-id="881c0-111">Impedir la migración de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="881c0-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="881c0-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="881c0-112">/NestedRestore</span></span>         | <span data-ttu-id="881c0-113">Cree un punto de restauración del sistema anidado.</span><span class="sxs-lookup"><span data-stu-id="881c0-113">Create a nested system restore point.</span></span> <span data-ttu-id="881c0-114">Úselo si la aplicación crea un punto de restauración del sistema para anidar el punto de restauración de Windows Media Player en el punto de restauración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="881c0-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="881c0-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="881c0-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="881c0-116">No permitir la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="881c0-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="881c0-117">Esta marca deshabilitará la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="881c0-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="881c0-118">En la mayoría de los casos, esta marca no debe usarse para la redistribución de software general.</span><span class="sxs-lookup"><span data-stu-id="881c0-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="881c0-119">Esto solo debe usarse cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos de Windows Media Player a una versión anterior del reproductor.</span><span class="sxs-lookup"><span data-stu-id="881c0-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="881c0-120">Esta marca solo se debe usar para la instalación corporativa o la instalación del fabricante de equipos originales (OEM).</span><span class="sxs-lookup"><span data-stu-id="881c0-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="881c0-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="881c0-121">/DefaultService</span></span>        | <span data-ttu-id="881c0-122">Establezca la tienda en línea inicial.</span><span class="sxs-lookup"><span data-stu-id="881c0-122">Set the initial online store.</span></span> <span data-ttu-id="881c0-123">Para obtener más información, consulte [configuración de parámetros de línea de comandos para tiendas en línea](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="881c0-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="881c0-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="881c0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="881c0-125">**Redistribuir el software de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="881c0-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="881c0-126">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="881c0-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




