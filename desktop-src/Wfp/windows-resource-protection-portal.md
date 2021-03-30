---
description: La protección de recursos impide el reemplazo de archivos y carpetas del sistema y las claves del registro esenciales para el sistema operativo. La modificación de los recursos protegidos puede producir un error del sistema o de la aplicación.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protección de recursos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361042"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="0d5d5-104">Protección de recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="0d5d5-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="0d5d5-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="0d5d5-105">Purpose</span></span>

<span data-ttu-id="0d5d5-106">Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="0d5d5-107">Estuvo disponible a partir de Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="0d5d5-108">Las aplicaciones no deben sobrescribir estos recursos porque son utilizados por el sistema y otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="0d5d5-109">La protección de estos recursos evita errores en la aplicación y en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="0d5d5-110">WRP es el nuevo nombre de protección de archivos de Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="0d5d5-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="0d5d5-111">WRP protege las claves del registro y las carpetas, así como los archivos esenciales del sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="0d5d5-112">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="0d5d5-112">Where applicable</span></span>

<span data-ttu-id="0d5d5-113">Todas las aplicaciones basadas en Windows y sus programas de instalación que se ejecutan en Windows Server 2008 o Windows Vista, y en los sistemas operativos posteriores, deben tener en cuenta WRP.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="0d5d5-114">Todas las aplicaciones basadas en Windows que se ejecutan en Microsoft Windows Server 2003 o Windows XP y sus programas de instalación deben tener en cuenta WFP.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0d5d5-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="0d5d5-115">Developer audience</span></span>

<span data-ttu-id="0d5d5-116">La API de WRP está diseñada para que la usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="0d5d5-117">La API de WRP tiene dos funciones: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="0d5d5-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0d5d5-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="0d5d5-118">Run-time requirements</span></span>

<span data-ttu-id="0d5d5-119">Las aplicaciones que usan solo la función [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) requieren windows Server 2008, Windows Vista, windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="0d5d5-120">Las aplicaciones que usan la función [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) requieren windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d5d5-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="0d5d5-121">In this section</span></span>



| <span data-ttu-id="0d5d5-122">Tema</span><span class="sxs-lookup"><span data-stu-id="0d5d5-122">Topic</span></span>                                                                                     | <span data-ttu-id="0d5d5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d5d5-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="0d5d5-124">Acerca de Protección de recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="0d5d5-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="0d5d5-125">Información general acerca de WRP.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="0d5d5-126">Referencia de Protección de recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="0d5d5-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="0d5d5-127">Documentación de referencia para WRP.</span><span class="sxs-lookup"><span data-stu-id="0d5d5-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




