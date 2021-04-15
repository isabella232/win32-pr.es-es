---
title: Copias de seguridad y restauración de Windows 7 en desuso
description: Copias de seguridad y restauración de Windows 7 en desuso
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105676515"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="0010f-103">Copias de seguridad y restauración de Windows 7 en desuso</span><span class="sxs-lookup"><span data-stu-id="0010f-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="0010f-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="0010f-104">Platform</span></span>

<span data-ttu-id="0010f-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="0010f-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="0010f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="0010f-106">Description</span></span>

<span data-ttu-id="0010f-107">Aunque no hay ningún cambio de comportamiento en la copia de seguridad y la restauración, esta función está en desuso y no se actualizará.</span><span class="sxs-lookup"><span data-stu-id="0010f-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="0010f-108">Rara vez se usaba y su funcionalidad se ha reemplazado por la nueva característica historial de archivos.</span><span class="sxs-lookup"><span data-stu-id="0010f-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="0010f-109">Se incluirá en Windows 8 y entusiastas que se hayan actualizado de Windows 7 a Windows 8 o que dependan de la copia de seguridad y la restauración, o bien que la copia de seguridad de la imagen de disco siga pudiendo usarla.</span><span class="sxs-lookup"><span data-stu-id="0010f-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="0010f-110">Sin embargo, se han quitado todos los puntos de acceso a la copia de seguridad y restauración, con la excepción del panel de control.</span><span class="sxs-lookup"><span data-stu-id="0010f-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="0010f-111">Se ha cambiado el nombre del applet del panel de control usado por copias de seguridad y restauración a recuperación de archivos de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0010f-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="0010f-112">Los OEM que establecieron la clave del registro para deshabilitar la notificación de copias de seguridad en sus imágenes ya no tendrán que hacerlo.</span><span class="sxs-lookup"><span data-stu-id="0010f-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="0010f-113">No se recomienda usar ambas características al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="0010f-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="0010f-114">El historial de archivos comprueba si existe una programación de copia de seguridad y está activa y, si encuentra alguna, no permitirá que los usuarios la activen.</span><span class="sxs-lookup"><span data-stu-id="0010f-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="0010f-115">En este caso, los usuarios que deseen usar el historial de archivos tendrán que eliminar la programación de copias de seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="0010f-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="0010f-116">Manifestación</span><span class="sxs-lookup"><span data-stu-id="0010f-116">Manifestation</span></span>

<span data-ttu-id="0010f-117">Los flujos de trabajo se pueden interrumpir y es necesario actualizar la documentación que hace referencia al método anterior para tener acceso a la característica copia de seguridad y restauración de Windows para reflejar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="0010f-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="0010f-118">Mitigación</span><span class="sxs-lookup"><span data-stu-id="0010f-118">Mitigation</span></span>

<span data-ttu-id="0010f-119">Las aplicaciones que pueden desencadenar copias de seguridad y restauración se deben volver a escribir para comprobar si el historial de archivos está activado y permitir que los usuarios elijan su método preferido.</span><span class="sxs-lookup"><span data-stu-id="0010f-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




