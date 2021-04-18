---
description: Recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: Propiedad BasicConstraints. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671412"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="4277f-103">Propiedad BasicConstraints. IsCritical</span><span class="sxs-lookup"><span data-stu-id="4277f-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="4277f-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4277f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4277f-105">En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="4277f-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4277f-106">La propiedad **IsCritical** recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="4277f-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="4277f-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4277f-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4277f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4277f-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4277f-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4277f-109">Property value</span></span>

<span data-ttu-id="4277f-110">Si es **true**, la extensión de restricción básica se marca como crítica.</span><span class="sxs-lookup"><span data-stu-id="4277f-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="4277f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4277f-111">Requirements</span></span>



| <span data-ttu-id="4277f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4277f-112">Requirement</span></span> | <span data-ttu-id="4277f-113">Value</span><span class="sxs-lookup"><span data-stu-id="4277f-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4277f-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4277f-114">End of client support</span></span><br/> | <span data-ttu-id="4277f-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4277f-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4277f-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4277f-116">End of server support</span></span><br/> | <span data-ttu-id="4277f-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4277f-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4277f-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4277f-118">Redistributable</span></span><br/>       | <span data-ttu-id="4277f-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4277f-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4277f-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4277f-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4277f-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4277f-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
