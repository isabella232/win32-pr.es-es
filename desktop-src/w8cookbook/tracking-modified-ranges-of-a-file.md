---
title: Seguimiento de los intervalos modificados de un archivo
description: Seguimiento de los intervalos modificados de un archivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705051"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="7635c-103">Seguimiento de los intervalos modificados de un archivo</span><span class="sxs-lookup"><span data-stu-id="7635c-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="7635c-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="7635c-104">Platforms</span></span>

<span data-ttu-id="7635c-105">**Clientes-** Windows 8.1 (todas las SKU)</span><span class="sxs-lookup"><span data-stu-id="7635c-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="7635c-106">**Servidores:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7635c-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="7635c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7635c-107">Description</span></span>

<span data-ttu-id="7635c-108">El equipo del sistema de archivos NT (NTFS) ha agregado una nueva característica a Windows.</span><span class="sxs-lookup"><span data-stu-id="7635c-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="7635c-109">El diario USN generará un registro de número de secuencia de actualización (USN) que contiene los intervalos modificados de un archivo al cerrarse.</span><span class="sxs-lookup"><span data-stu-id="7635c-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="7635c-110">Se ha introducido un nuevo tipo de registro, el \_ registro USN \_ V4 para registrar estos intervalos modificados de un archivo.</span><span class="sxs-lookup"><span data-stu-id="7635c-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="7635c-111">La característica no está habilitada de forma predeterminada; los usuarios deben invocar un comando de control del sistema de archivos (FSCTL) para habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="7635c-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="7635c-112">Sin embargo, dado que otros componentes de Windows pueden activar el seguimiento de intervalos, los usuarios y los desarrolladores pueden percibir que la característica está siempre habilitada.</span><span class="sxs-lookup"><span data-stu-id="7635c-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="7635c-113">Windows permitirá a los desarrolladores consultar el diario USN para averiguar si está habilitado el seguimiento de intervalo.</span><span class="sxs-lookup"><span data-stu-id="7635c-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="7635c-114">La documentación de MSDN se proporcionará en una fecha posterior para instruir a los desarrolladores sobre cómo acceder a \_ los registros de registro de USN \_ V4.</span><span class="sxs-lookup"><span data-stu-id="7635c-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7635c-115">Manifestación</span><span class="sxs-lookup"><span data-stu-id="7635c-115">Manifestation</span></span>

<span data-ttu-id="7635c-116">Todas las aplicaciones existentes que usan el diario USN seguirán funcionando bien sin problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="7635c-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 




