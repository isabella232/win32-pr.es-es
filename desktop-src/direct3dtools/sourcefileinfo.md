---
description: Representa información sobre un archivo de código fuente.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura SourceFileInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495245"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="a287e-103"><span id="vspixengine.sourcefileinfo"></span>Estructura SourceFileInfo</span><span class="sxs-lookup"><span data-stu-id="a287e-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="a287e-104">Representa información sobre un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="a287e-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a287e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a287e-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="a287e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a287e-106">Members</span></span>

<span data-ttu-id="a287e-107">**fileName**</span><span class="sxs-lookup"><span data-stu-id="a287e-107">**fileName**</span></span>  
<span data-ttu-id="a287e-108">Una cadena COM comtaining la ruta de acceso del archivo de código fuente asociado.</span><span class="sxs-lookup"><span data-stu-id="a287e-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="a287e-109">**checksumByteCount**</span><span class="sxs-lookup"><span data-stu-id="a287e-109">**checksumByteCount**</span></span>  
<span data-ttu-id="a287e-110">Número de bytes de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a287e-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="a287e-111">Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM:: MD5, checkSumByteCount es 16.</span><span class="sxs-lookup"><span data-stu-id="a287e-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="a287e-112">Cuando checkSumAlgorithm es igual a CHECKSUMALGORITHM:: SHA1, checkSumByteCount es 20.</span><span class="sxs-lookup"><span data-stu-id="a287e-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="a287e-113">**checkSumAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="a287e-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="a287e-114">Especifica el algoritmo utilizado para generar la suma de comprobación del archivo.</span><span class="sxs-lookup"><span data-stu-id="a287e-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="a287e-115">Los algoritmos admitidos son MD5 y SHA1.</span><span class="sxs-lookup"><span data-stu-id="a287e-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="a287e-116">Para obtener más información, consulte la enumeración CHECKSUMALGORITHM.</span><span class="sxs-lookup"><span data-stu-id="a287e-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="a287e-117">**checkSumFirstPart**</span><span class="sxs-lookup"><span data-stu-id="a287e-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="a287e-118">La primera parte de 8 bytes de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a287e-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="a287e-119">**checkSumSecondPart**</span><span class="sxs-lookup"><span data-stu-id="a287e-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="a287e-120">La segunda parte de 8 bytes de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a287e-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="a287e-121">**checkSumThirdPart**</span><span class="sxs-lookup"><span data-stu-id="a287e-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="a287e-122">La tercera parte de 8 bytes de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a287e-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="a287e-123">**checkSumFourthPart**</span><span class="sxs-lookup"><span data-stu-id="a287e-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="a287e-124">Cuarta parte de 8 bytes de la suma de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a287e-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="a287e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a287e-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a287e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a287e-126">Header</span></span></p></td><td><span data-ttu-id="a287e-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a287e-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



