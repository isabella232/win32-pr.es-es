---
description: La \_ estructura ADDJOB info \_ 1 identifica un trabajo de impresión, así como el directorio y el archivo en el que una aplicación puede almacenar ese trabajo.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Estructura de ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279034"
---
# <a name="addjob_info_1-structure"></a><span data-ttu-id="cc801-103">ADDJOB \_ estructura de información \_ 1</span><span class="sxs-lookup"><span data-stu-id="cc801-103">ADDJOB\_INFO\_1 structure</span></span>

<span data-ttu-id="cc801-104">La estructura **ADDJOB \_ info \_ 1** identifica un trabajo de impresión, así como el directorio y el archivo en el que una aplicación puede almacenar ese trabajo.</span><span class="sxs-lookup"><span data-stu-id="cc801-104">The **ADDJOB\_INFO\_1** structure identifies a print job as well as the directory and file in which an application can store that job.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc801-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc801-105">Syntax</span></span>


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a><span data-ttu-id="cc801-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc801-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc801-107">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="cc801-107">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="cc801-108">Puntero a una cadena terminada en null que contiene la ruta de acceso y el nombre de archivo que la aplicación puede usar para almacenar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="cc801-108">Pointer to a null-terminated string that contains the path and file name that the application can use to store the print job.</span></span>

</dd> <dt>

<span data-ttu-id="cc801-109">**JobId**</span><span class="sxs-lookup"><span data-stu-id="cc801-109">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="cc801-110">Identificador del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="cc801-110">A handle to the print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc801-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc801-111">Requirements</span></span>



| <span data-ttu-id="cc801-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc801-112">Requirement</span></span> | <span data-ttu-id="cc801-113">Value</span><span class="sxs-lookup"><span data-stu-id="cc801-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc801-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc801-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cc801-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cc801-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cc801-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc801-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cc801-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc801-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cc801-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc801-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc801-119"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc801-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cc801-120">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="cc801-120">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cc801-121">**\_ ADDJOB \_ info \_ 1W** (Unicode) y **\_ ADDJOB \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cc801-121">**\_ADDJOB\_INFO\_1W** (Unicode) and **\_ADDJOB\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="cc801-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc801-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc801-123">Impresión</span><span class="sxs-lookup"><span data-stu-id="cc801-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cc801-124">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="cc801-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="cc801-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="cc801-125">**AddJob**</span></span>](addjob.md)
</dt> </dl>

 

 




