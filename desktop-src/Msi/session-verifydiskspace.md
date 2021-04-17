---
description: La propiedad VerifyDiskSpace es una propiedad de solo lectura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Propiedad Session. VerifyDiskSpace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681120"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="7b0d5-103">Propiedad Session. VerifyDiskSpace</span><span class="sxs-lookup"><span data-stu-id="7b0d5-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="7b0d5-104">La propiedad **VerifyDiskSpace** es una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b0d5-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="7b0d5-105">Devuelve true si existe suficiente espacio en disco y false si el disco está lleno.</span><span class="sxs-lookup"><span data-stu-id="7b0d5-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="7b0d5-106">Dado que esta propiedad usa la información recopilada por las acciones de costo, solo se debe llamar a **VerifyDiskSpace** después de la acción [CostInitialize](costinitialize-action.md), la [acción FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="7b0d5-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="7b0d5-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7b0d5-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b0d5-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="7b0d5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7b0d5-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0d5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b0d5-110">Requirements</span></span>



| <span data-ttu-id="7b0d5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0d5-111">Requirement</span></span> | <span data-ttu-id="7b0d5-112">Value</span><span class="sxs-lookup"><span data-stu-id="7b0d5-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0d5-113">Versión</span><span class="sxs-lookup"><span data-stu-id="7b0d5-113">Version</span></span><br/> | <span data-ttu-id="7b0d5-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b0d5-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b0d5-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b0d5-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b0d5-116">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b0d5-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7b0d5-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b0d5-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b0d5-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b0d5-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7b0d5-119">IID</span><span class="sxs-lookup"><span data-stu-id="7b0d5-119">IID</span></span><br/>     | <span data-ttu-id="7b0d5-120">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7b0d5-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




