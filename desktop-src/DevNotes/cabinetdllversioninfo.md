---
description: CABINETDLLVERSIONINFO contiene la información de versión de Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Estructura CABINETDLLVERSIONINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907170"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="a7cb6-103">Estructura CABINETDLLVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="a7cb6-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="a7cb6-104">\[Esta estructura contiene información necesaria solo cuando se usa la función **DllGetVersion** , que no se admite.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="a7cb6-105">Esta documentación se proporciona solo con fines informativos.\]</span><span class="sxs-lookup"><span data-stu-id="a7cb6-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="a7cb6-106">**CABINETDLLVERSIONINFO** contiene la información de versión de Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cb6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7cb6-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="a7cb6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7cb6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7cb6-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="a7cb6-110">Tamaño de esta estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb6-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="a7cb6-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb6-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="a7cb6-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb6-115">**dwFileVersionMS**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="a7cb6-116">Contiene los bits más significativos de la información de versión.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="a7cb6-117">Los bits 0-15 contienen la versión secundaria y los bits 16-31 contienen la versión principal.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="a7cb6-118">**dwFileVersionLS**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="a7cb6-119">Contiene los bits menos significativos de la información de versión.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="a7cb6-120">Los bits 0-15 contienen el número de revisión y los bits 16-31 contienen el número de compilación.</span><span class="sxs-lookup"><span data-stu-id="a7cb6-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a7cb6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7cb6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cb6-122">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="a7cb6-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



