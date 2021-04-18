---
description: Recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: SystemPrng función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666425"
---
# <a name="systemprng-function"></a><span data-ttu-id="28ad1-103">SystemPrng función)</span><span class="sxs-lookup"><span data-stu-id="28ad1-103">SystemPrng function</span></span>

<span data-ttu-id="28ad1-104">\[**SystemPrng** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="28ad1-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="28ad1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="28ad1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="28ad1-106">En su lugar, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="28ad1-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="28ad1-107">La función **SystemPrng** recupera un número especificado de bytes aleatorios del generador de números aleatorios del sistema.</span><span class="sxs-lookup"><span data-stu-id="28ad1-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="28ad1-108">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="28ad1-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="28ad1-109">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="28ad1-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="28ad1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28ad1-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="28ad1-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28ad1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ad1-112">*pbRandomData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28ad1-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28ad1-113">Puntero a un búfer que recibe los bytes recuperados.</span><span class="sxs-lookup"><span data-stu-id="28ad1-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="28ad1-114">*cbRandomData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28ad1-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ad1-115">El número de bytes que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="28ad1-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ad1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28ad1-116">Return value</span></span>

<span data-ttu-id="28ad1-117">Siempre devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="28ad1-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ad1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ad1-118">Requirements</span></span>



| <span data-ttu-id="28ad1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ad1-119">Requirement</span></span> | <span data-ttu-id="28ad1-120">Value</span><span class="sxs-lookup"><span data-stu-id="28ad1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ad1-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ad1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28ad1-122">Solo aplicaciones de escritorio con SP1 de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="28ad1-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="28ad1-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ad1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28ad1-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="28ad1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="28ad1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28ad1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28ad1-126"><dt>Ksecdd.sys en Windows Server 2008 y Windows Vista con SP1; </dt> <dt>Cng.sys en Windows 7 y Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="28ad1-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




