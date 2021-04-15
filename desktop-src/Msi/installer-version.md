---
description: La propiedad version del objeto Installer es una propiedad de solo lectura que es la representación de cadena de la versión actual de Windows Installer. La cadena se devuelve en el formato siguiente.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Propiedad Installer. version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653885"
---
# <a name="installerversion-property"></a><span data-ttu-id="64bf0-104">Propiedad Installer. version</span><span class="sxs-lookup"><span data-stu-id="64bf0-104">Installer.Version property</span></span>

<span data-ttu-id="64bf0-105">La propiedad **version** del objeto [**Installer**](installer-object.md) es una propiedad de solo lectura que es la representación de cadena de la versión actual de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="64bf0-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="64bf0-106">La cadena se devuelve en el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="64bf0-106">The string is returned in the following form.</span></span>

<span data-ttu-id="64bf0-107">*principal*. *secundaria*. *compilación*. *actualización* de</span><span class="sxs-lookup"><span data-stu-id="64bf0-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="64bf0-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64bf0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="64bf0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64bf0-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="64bf0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="64bf0-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="64bf0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64bf0-111">Requirements</span></span>



| <span data-ttu-id="64bf0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="64bf0-112">Requirement</span></span> | <span data-ttu-id="64bf0-113">Value</span><span class="sxs-lookup"><span data-stu-id="64bf0-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64bf0-114">Versión</span><span class="sxs-lookup"><span data-stu-id="64bf0-114">Version</span></span><br/> | <span data-ttu-id="64bf0-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64bf0-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64bf0-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64bf0-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64bf0-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="64bf0-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="64bf0-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64bf0-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="64bf0-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64bf0-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="64bf0-120">IID</span><span class="sxs-lookup"><span data-stu-id="64bf0-120">IID</span></span><br/>     | <span data-ttu-id="64bf0-121">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="64bf0-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




