---
description: La propiedad SummaryInformation del objeto de instalador devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de Resumen de un paquete o transformación.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Propiedad Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653386"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="03301-103">Propiedad Installer. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="03301-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="03301-104">La propiedad **SummaryInformation** del objeto de [**instalador**](installer-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de Resumen de un paquete o transformación.</span><span class="sxs-lookup"><span data-stu-id="03301-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="03301-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="03301-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03301-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03301-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="03301-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="03301-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="03301-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03301-108">Remarks</span></span>

<span data-ttu-id="03301-109">Si se usa un valor de *maxProperties* mayor que 0 para abrir una secuencia de información de Resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto.</span><span class="sxs-lookup"><span data-stu-id="03301-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="03301-110">Si no lo hace, se pierde la información de la secuencia existente.</span><span class="sxs-lookup"><span data-stu-id="03301-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03301-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03301-111">Requirements</span></span>



| <span data-ttu-id="03301-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="03301-112">Requirement</span></span> | <span data-ttu-id="03301-113">Value</span><span class="sxs-lookup"><span data-stu-id="03301-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03301-114">Versión</span><span class="sxs-lookup"><span data-stu-id="03301-114">Version</span></span><br/> | <span data-ttu-id="03301-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03301-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03301-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03301-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03301-117">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="03301-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="03301-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03301-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="03301-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03301-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="03301-120">IID</span><span class="sxs-lookup"><span data-stu-id="03301-120">IID</span></span><br/>     | <span data-ttu-id="03301-121">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03301-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




