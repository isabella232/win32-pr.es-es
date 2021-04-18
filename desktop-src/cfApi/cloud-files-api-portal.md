---
description: Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motores de sincronización en la nube
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/20/2021
ms.locfileid: "105718594"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="6a7f0-103">Motores de sincronización en la nube</span><span class="sxs-lookup"><span data-stu-id="6a7f0-103">Cloud Sync Engines</span></span>

<span data-ttu-id="6a7f0-104">Vea también [ejemplo de reflejo en la nube](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="6a7f0-104">Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span></span>

<span data-ttu-id="6a7f0-105">A partir de Windows 10, versión 1709, Windows proporciona la *API de archivos* en la nube.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="6a7f0-106">Esta API está compuesta de varias API nativas de Win32 y WinRT que formalizan la compatibilidad con los motores de sincronización en la nube y administran tareas como la creación y administración de archivos y directorios de marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="6a7f0-107">Los usuarios de esta API suelen ser proveedores de sincronización y, en cierto grado, aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6a7f0-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6a7f0-108">In this section</span></span>

| <span data-ttu-id="6a7f0-109">Tema</span><span class="sxs-lookup"><span data-stu-id="6a7f0-109">Topic</span></span>                                                                | <span data-ttu-id="6a7f0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a7f0-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a7f0-111">Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="6a7f0-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="6a7f0-112">Aprenda a usar la API de archivos en la nube para crear un motor de sincronización de archivos en la nube que incluya archivos de marcadores de posición e integración con el explorador de archivos.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="6a7f0-113">Referencia de filtro de nube</span><span class="sxs-lookup"><span data-stu-id="6a7f0-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="6a7f0-114">Cloud Filter API es una API nativa de Win32 que forma parte de la API de archivos en la nube más amplia.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="6a7f0-115">Cloud Filter API proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="6a7f0-116">Esta API controla la creación y administración de archivos y directorios de marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="6a7f0-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |

