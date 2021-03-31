---
description: La \_ estructura PROVIDOR info \_ 1 identifica un proveedor de impresión.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Estructura de PROVIDOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361096"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="09d73-103">PROVIDOR \_ estructura de información \_ 1</span><span class="sxs-lookup"><span data-stu-id="09d73-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="09d73-104">La estructura **PROVIDOR \_ info \_ 1** identifica un proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="09d73-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09d73-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="09d73-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="09d73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="09d73-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="09d73-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="09d73-108">Puntero a una cadena terminada en null que es el nombre del proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="09d73-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="09d73-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="09d73-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="09d73-110">Puntero a una cadena de entorno terminada en null que especifica el entorno en el que se ha diseñado la biblioteca de vínculos dinámicos (DLL) del proveedor.</span><span class="sxs-lookup"><span data-stu-id="09d73-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="09d73-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="09d73-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="09d73-112">Puntero a una cadena terminada en null que es el nombre de Provider. dll.</span><span class="sxs-lookup"><span data-stu-id="09d73-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09d73-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09d73-113">Requirements</span></span>



| <span data-ttu-id="09d73-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d73-114">Requirement</span></span> | <span data-ttu-id="09d73-115">Value</span><span class="sxs-lookup"><span data-stu-id="09d73-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d73-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="09d73-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09d73-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="09d73-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="09d73-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09d73-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="09d73-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09d73-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d73-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09d73-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="09d73-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="09d73-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="09d73-123">**\_ PROVIDOR \_ info \_ 1W** (Unicode) y **\_ PROVIDOR \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="09d73-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="09d73-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="09d73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d73-125">Impresión</span><span class="sxs-lookup"><span data-stu-id="09d73-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="09d73-126">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="09d73-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="09d73-127">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="09d73-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




