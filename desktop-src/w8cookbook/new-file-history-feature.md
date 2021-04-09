---
title: Nueva característica de historial de archivos
description: Nueva característica de historial de archivos
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104149688"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="3273d-103">Nueva característica de historial de archivos</span><span class="sxs-lookup"><span data-stu-id="3273d-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="3273d-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="3273d-104">Platform</span></span>

<span data-ttu-id="3273d-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="3273d-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="3273d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3273d-106">Description</span></span>

<span data-ttu-id="3273d-107">La nueva característica de historial de archivos reemplaza a la función de copia de seguridad y restauración existente y ofrece protección para los archivos de usuario almacenados en las bibliotecas de usuario.</span><span class="sxs-lookup"><span data-stu-id="3273d-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="3273d-108">Se proporciona un conjunto de API que permite a los desarrolladores habilitar mediante programación el historial de archivos y seleccionar un destino de almacenamiento específico.</span><span class="sxs-lookup"><span data-stu-id="3273d-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="3273d-109">La documentación de estas API está disponible en MSDN.</span><span class="sxs-lookup"><span data-stu-id="3273d-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="3273d-110">Puede afectar a los flujos de trabajo relacionados con la protección de datos y la documentación que dependen de la característica copia de seguridad y restauración de Windows.</span><span class="sxs-lookup"><span data-stu-id="3273d-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="3273d-111">No se recomienda usar ambas características al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="3273d-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="3273d-112">El historial de archivos comprueba si existe una programación de copia de seguridad y está activa y, si encuentra alguna, no permitirá que los usuarios la activen.</span><span class="sxs-lookup"><span data-stu-id="3273d-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="3273d-113">En este caso, los usuarios que deseen usar el historial de archivos tendrán que eliminar la programación de copias de seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="3273d-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="3273d-114">Manifestación</span><span class="sxs-lookup"><span data-stu-id="3273d-114">Manifestation</span></span>

<span data-ttu-id="3273d-115">Los flujos de trabajo se pueden interrumpir y la documentación del método anterior para tener acceso a la característica copia de seguridad y restauración de Windows deberá actualizarse para reflejar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="3273d-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="3273d-116">Solución</span><span class="sxs-lookup"><span data-stu-id="3273d-116">Solution</span></span>

<span data-ttu-id="3273d-117">Revise las aplicaciones que contienen flujos de trabajo que se ven perjudicados por la nueva característica de historial de archivos para quitar los conflictos e incorporar el nuevo conjunto de API.</span><span class="sxs-lookup"><span data-stu-id="3273d-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="3273d-118">Pruebas</span><span class="sxs-lookup"><span data-stu-id="3273d-118">Tests</span></span>

<span data-ttu-id="3273d-119">La API permite a los desarrolladores determinar si el historial de archivos está activado.</span><span class="sxs-lookup"><span data-stu-id="3273d-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




