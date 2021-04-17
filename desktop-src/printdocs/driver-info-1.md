---
description: La estructura de la información del controlador \_ \_ 1 identifica un controlador de impresora.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Estructura de DRIVER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716798"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="90ca7-103">Estructura de información de controlador \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="90ca7-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="90ca7-104">La estructura de la **información del controlador \_ \_ 1** identifica un controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="90ca7-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ca7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90ca7-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="90ca7-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="90ca7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90ca7-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="90ca7-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="90ca7-108">Puntero a una cadena terminada en null que especifica el nombre de un controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="90ca7-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90ca7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90ca7-109">Requirements</span></span>



| <span data-ttu-id="90ca7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ca7-110">Requirement</span></span> | <span data-ttu-id="90ca7-111">Value</span><span class="sxs-lookup"><span data-stu-id="90ca7-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ca7-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ca7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="90ca7-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90ca7-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="90ca7-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ca7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="90ca7-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90ca7-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="90ca7-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90ca7-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ca7-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90ca7-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="90ca7-118">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="90ca7-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="90ca7-119">**\_ Información del controlador \_ \_ 1W** (Unicode) y la **\_ información del controlador \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="90ca7-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="90ca7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="90ca7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ca7-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="90ca7-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="90ca7-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="90ca7-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="90ca7-123">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="90ca7-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




