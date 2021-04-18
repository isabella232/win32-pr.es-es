---
description: La \_ estructura PROVIDOR info \_ 2 anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Estructura de PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688234"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="f1e97-103">Estructura de PROVIDOR \_ info \_ 2</span><span class="sxs-lookup"><span data-stu-id="f1e97-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="f1e97-104">La estructura **PROVIDOR \_ info \_ 2** anexa un proveedor de impresión a la lista de pedidos del proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="f1e97-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1e97-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f1e97-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1e97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1e97-107">**pOrder**</span><span class="sxs-lookup"><span data-stu-id="f1e97-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="f1e97-108">Puntero a una cadena terminada en null que especifica el nombre del proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="f1e97-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1e97-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1e97-109">Remarks</span></span>

<span data-ttu-id="f1e97-110">Esta estructura se usa al llamar a [**AddPrintProvidor**](addprintprovidor.md), nivel 2, para agregar el proveedor de impresión especificado al final de la lista de pedidos del proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="f1e97-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="f1e97-111">El proveedor se usa inmediatamente para el enrutamiento si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f1e97-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e97-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1e97-112">Requirements</span></span>



| <span data-ttu-id="f1e97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e97-113">Requirement</span></span> | <span data-ttu-id="f1e97-114">Value</span><span class="sxs-lookup"><span data-stu-id="f1e97-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e97-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1e97-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e97-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f1e97-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1e97-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1e97-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e97-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f1e97-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1e97-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1e97-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e97-120"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1e97-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f1e97-121">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f1e97-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1e97-122">**\_ PROVIDOR \_ info \_ 2W** (Unicode) y **\_ PROVIDOR \_ info \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f1e97-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="f1e97-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1e97-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e97-124">Impresión</span><span class="sxs-lookup"><span data-stu-id="f1e97-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f1e97-125">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f1e97-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f1e97-126">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="f1e97-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




