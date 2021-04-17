---
title: StorAHCI reemplaza a MSAHCI
description: StorAHCI reemplaza a MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105705055"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="4ee1a-103">StorAHCI reemplaza a MSAHCI</span><span class="sxs-lookup"><span data-stu-id="4ee1a-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="4ee1a-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="4ee1a-104">Platforms</span></span>

<span data-ttu-id="4ee1a-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ee1a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="4ee1a-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ee1a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="4ee1a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ee1a-107">Description</span></span>

<span data-ttu-id="4ee1a-108">StorAHCI, un minipuerto Storport, es compatible con los controladores de la interfaz de controlador de hosts (AHCI) avanzada de Serial Advanced Technology Attachment (SATA) en Windows y reemplaza MSAHCI, un minipuerto ATAport.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="4ee1a-109">Manifestación</span><span class="sxs-lookup"><span data-stu-id="4ee1a-109">Manifestation</span></span>

<span data-ttu-id="4ee1a-110">No debe haber ningún cambio en la funcionalidad o el rendimiento; Este controlador es compatible con todos los dispositivos que admite MSAHCI.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="4ee1a-111">Este cambio es transparente para el usuario.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4ee1a-112">Mitigación</span><span class="sxs-lookup"><span data-stu-id="4ee1a-112">Mitigation</span></span>

<span data-ttu-id="4ee1a-113">Actualice las utilidades y los scripts que se basan en los enlaces de ATAport.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="4ee1a-114">No se base en el nombre de la unidad.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-114">Do not rely on the drive name.</span></span> <span data-ttu-id="4ee1a-115">En su lugar, use la detección de disco estándar.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-115">Instead use standard disk detection.</span></span>

 

 




