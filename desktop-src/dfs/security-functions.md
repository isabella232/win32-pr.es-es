---
title: Funciones de seguridad
description: Las funciones de seguridad de administración de redes obtienen y establecen descriptores de seguridad para las raíces basadas en dominio DFS y independientes.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496637"
---
# <a name="security-functions"></a><span data-ttu-id="51b66-103">Funciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="51b66-103">Security Functions</span></span>

<span data-ttu-id="51b66-104">Las funciones de seguridad de administración de redes obtienen y establecen descriptores de seguridad para las raíces basadas en dominio DFS y independientes.</span><span class="sxs-lookup"><span data-stu-id="51b66-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="51b66-105">A continuación se enumeran las funciones de seguridad de DFS.</span><span class="sxs-lookup"><span data-stu-id="51b66-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="51b66-106">Función</span><span class="sxs-lookup"><span data-stu-id="51b66-106">Function</span></span>                                                               | <span data-ttu-id="51b66-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="51b66-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51b66-108">**NetDfsGetSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="51b66-109">Obtiene el descriptor de seguridad para el objeto raíz de la raíz DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="51b66-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="51b66-110">**NetDfsSetSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="51b66-111">Busca el objeto raíz de la raíz DFS especificada y establece el descriptor de seguridad proporcionado en él.</span><span class="sxs-lookup"><span data-stu-id="51b66-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="51b66-112">**NetDfsGetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="51b66-113">Obtiene el descriptor de seguridad para el objeto contenedor de la raíz independiente DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="51b66-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="51b66-114">**NetDfsSetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="51b66-115">Busca el objeto contenedor de la raíz independiente DFS especificada y establece el descriptor de seguridad proporcionado en él.</span><span class="sxs-lookup"><span data-stu-id="51b66-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="51b66-116">**NetDfsGetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="51b66-117">Obtiene el descriptor de seguridad para el objeto contenedor de la raíz de dominio DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="51b66-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="51b66-118">**NetDfsSetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="51b66-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="51b66-119">Busca el objeto contenedor para la raíz de dominio DFS especificada y establece el descriptor de seguridad proporcionado en él.</span><span class="sxs-lookup"><span data-stu-id="51b66-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
