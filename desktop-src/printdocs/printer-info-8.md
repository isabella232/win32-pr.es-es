---
description: La estructura de la información de la impresora \_ \_ 8 especifica la configuración de impresora predeterminada global.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Estructura de PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912958"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="53b7b-103">Información de impresora \_ \_ 8 (estructura)</span><span class="sxs-lookup"><span data-stu-id="53b7b-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="53b7b-104">La estructura de la información de la **impresora \_ \_ 8** especifica la configuración de impresora predeterminada global.</span><span class="sxs-lookup"><span data-stu-id="53b7b-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b7b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53b7b-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="53b7b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="53b7b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53b7b-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="53b7b-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="53b7b-108">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados globales, como la orientación del papel y la resolución.</span><span class="sxs-lookup"><span data-stu-id="53b7b-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53b7b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53b7b-109">Remarks</span></span>

<span data-ttu-id="53b7b-110">Los valores predeterminados globales están establecidos por el administrador de una impresora que puede usar cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="53b7b-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="53b7b-111">Por el contrario, los valores predeterminados por usuario afectarán a un usuario determinado o a cualquier otra persona que use el perfil.</span><span class="sxs-lookup"><span data-stu-id="53b7b-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="53b7b-112">Para los valores predeterminados por usuario, use la información de la [**impresora \_ \_ 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="53b7b-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53b7b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53b7b-113">Requirements</span></span>



| <span data-ttu-id="53b7b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53b7b-114">Requirement</span></span> | <span data-ttu-id="53b7b-115">Value</span><span class="sxs-lookup"><span data-stu-id="53b7b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b7b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53b7b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53b7b-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53b7b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53b7b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53b7b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53b7b-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="53b7b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53b7b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53b7b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53b7b-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53b7b-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="53b7b-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="53b7b-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53b7b-123">Información de la **\_ impresora \_ \_ 8W** (Unicode) y la información de la **\_ impresora \_ \_ 8A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="53b7b-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="53b7b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="53b7b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b7b-125">Impresión</span><span class="sxs-lookup"><span data-stu-id="53b7b-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="53b7b-126">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="53b7b-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="53b7b-127">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="53b7b-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="53b7b-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="53b7b-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="53b7b-129">**Información de la impresora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="53b7b-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




