---
description: La estructura de la información de la impresora \_ \_ 9 especifica la configuración de impresora predeterminada por usuario.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Estructura de PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720722"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="15822-103">Estructura de información de la impresora \_ \_ 9</span><span class="sxs-lookup"><span data-stu-id="15822-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="15822-104">La estructura de la información de la **impresora \_ \_ 9** especifica la configuración de impresora predeterminada por usuario.</span><span class="sxs-lookup"><span data-stu-id="15822-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="15822-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15822-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="15822-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="15822-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15822-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="15822-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="15822-108">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados por usuario, como la orientación del papel y la resolución.</span><span class="sxs-lookup"><span data-stu-id="15822-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="15822-109">El **DEVMODE** se almacena en el registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="15822-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15822-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15822-110">Remarks</span></span>

<span data-ttu-id="15822-111">Los valores predeterminados por usuario solo afectarán a un usuario determinado o a cualquiera que use el perfil.</span><span class="sxs-lookup"><span data-stu-id="15822-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="15822-112">En cambio, los valores predeterminados globales están establecidos por el administrador de una impresora que puede usar cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="15822-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="15822-113">Para los valores predeterminados globales, use la información de la [**impresora \_ \_ 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="15822-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15822-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15822-114">Requirements</span></span>



| <span data-ttu-id="15822-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15822-115">Requirement</span></span> | <span data-ttu-id="15822-116">Value</span><span class="sxs-lookup"><span data-stu-id="15822-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15822-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15822-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15822-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="15822-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15822-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15822-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15822-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15822-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15822-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15822-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15822-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15822-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="15822-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="15822-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15822-124">Información de la **\_ impresora \_ \_ 9W** (Unicode) e información de la **\_ impresora \_ \_ 9 bis** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="15822-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="15822-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="15822-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15822-126">Impresión</span><span class="sxs-lookup"><span data-stu-id="15822-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="15822-127">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="15822-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="15822-128">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="15822-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="15822-129">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="15822-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="15822-130">**Información de la impresora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="15822-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




