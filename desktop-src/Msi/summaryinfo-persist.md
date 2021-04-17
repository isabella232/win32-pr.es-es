---
description: El método Persist de los formatos de objeto SummaryInfo y escribe las propiedades previamente almacenadas en el flujo SummaryInformation estándar.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. Persist (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680434"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="52c20-103">SummaryInfo. Persist (método)</span><span class="sxs-lookup"><span data-stu-id="52c20-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="52c20-104">El método **Persist** de los formatos de objeto [**SummaryInfo**](summaryinfo-object.md) y escribe las propiedades previamente almacenadas en el flujo SummaryInformation estándar.</span><span class="sxs-lookup"><span data-stu-id="52c20-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="52c20-105">Genera un error si la secuencia no se puede escribir correctamente.</span><span class="sxs-lookup"><span data-stu-id="52c20-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="52c20-106">Solo se puede llamar una vez a este método una vez que se han establecido todos los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="52c20-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="52c20-107">Todavía se pueden leer las propiedades después de escribir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="52c20-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c20-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52c20-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="52c20-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52c20-109">Parameters</span></span>

<span data-ttu-id="52c20-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="52c20-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="52c20-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52c20-111">Return value</span></span>

<span data-ttu-id="52c20-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="52c20-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c20-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c20-113">Requirements</span></span>



| <span data-ttu-id="52c20-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c20-114">Requirement</span></span> | <span data-ttu-id="52c20-115">Value</span><span class="sxs-lookup"><span data-stu-id="52c20-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c20-116">Versión</span><span class="sxs-lookup"><span data-stu-id="52c20-116">Version</span></span><br/> | <span data-ttu-id="52c20-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52c20-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52c20-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52c20-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52c20-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="52c20-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="52c20-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52c20-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="52c20-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52c20-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="52c20-122">IID</span><span class="sxs-lookup"><span data-stu-id="52c20-122">IID</span></span><br/>     | <span data-ttu-id="52c20-123">IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="52c20-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




