---
description: La estructura de la información de la impresora \_ \_ 3 especifica información de seguridad de la impresora.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Estructura de PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720654"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="8a4e0-103">Estructura de la información de la impresora \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="8a4e0-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="8a4e0-104">La estructura de la información de la **impresora \_ \_ 3** especifica información de seguridad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8a4e0-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a4e0-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="8a4e0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a4e0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a4e0-107">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="8a4e0-108">Puntero a una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que especifica la información de seguridad de una impresora.</span><span class="sxs-lookup"><span data-stu-id="8a4e0-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a4e0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a4e0-109">Remarks</span></span>

<span data-ttu-id="8a4e0-110">La estructura de la información de la **impresora \_ \_ 3** permite a una aplicación obtener y establecer el descriptor de seguridad de una impresora.</span><span class="sxs-lookup"><span data-stu-id="8a4e0-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="8a4e0-111">El autor de la llamada puede hacerlo incluso si carece de permisos de impresora específicos, siempre y cuando tenga los derechos estándar descritos en [**SetPrinter**](setprinter.md) y [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e0-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="8a4e0-112">Por lo tanto, una aplicación puede denegar temporalmente el acceso a una impresora, a la vez que permite que el propietario de la impresora tenga acceso a la ACL discrecional de la impresora.</span><span class="sxs-lookup"><span data-stu-id="8a4e0-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a4e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a4e0-113">Requirements</span></span>



| <span data-ttu-id="8a4e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a4e0-114">Requirement</span></span> | <span data-ttu-id="8a4e0-115">Value</span><span class="sxs-lookup"><span data-stu-id="8a4e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4e0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a4e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8a4e0-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8a4e0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8a4e0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a4e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8a4e0-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a4e0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a4e0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a4e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a4e0-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4e0-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a4e0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a4e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4e0-123">Impresión</span><span class="sxs-lookup"><span data-stu-id="8a4e0-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-124">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="8a4e0-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-125">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-126">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-127">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-128">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-129">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="8a4e0-130">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="8a4e0-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

