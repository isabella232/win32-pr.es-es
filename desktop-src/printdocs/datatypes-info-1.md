---
description: La estructura de información de tipos de \_ \_ datos 1 contiene información sobre el tipo de datos utilizado para registrar un trabajo de impresión.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Estructura de DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276787"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="88b02-103">Estructura de información de tipos de \_ dato \_ 1</span><span class="sxs-lookup"><span data-stu-id="88b02-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="88b02-104">La estructura de información de tipos de datos **\_ \_ 1** contiene información sobre el tipo de datos utilizado para registrar un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="88b02-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88b02-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="88b02-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="88b02-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88b02-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="88b02-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="88b02-108">Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="88b02-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88b02-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b02-109">Requirements</span></span>



| <span data-ttu-id="88b02-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="88b02-110">Requirement</span></span> | <span data-ttu-id="88b02-111">Value</span><span class="sxs-lookup"><span data-stu-id="88b02-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b02-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88b02-112">Minimum supported client</span></span><br/> | <span data-ttu-id="88b02-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="88b02-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88b02-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88b02-114">Minimum supported server</span></span><br/> | <span data-ttu-id="88b02-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="88b02-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88b02-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88b02-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="88b02-117"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88b02-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="88b02-118">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="88b02-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="88b02-119">**\_ Información de tipos de \_ dato \_ 1W** (Unicode) e **\_ información sobre tipos de \_ dato \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="88b02-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="88b02-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="88b02-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b02-121">Impresión</span><span class="sxs-lookup"><span data-stu-id="88b02-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="88b02-122">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="88b02-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="88b02-123">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="88b02-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




