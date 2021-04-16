---
description: La \_ estructura doc info \_ 3 describe un documento que se va a imprimir.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Estructura de DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716032"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="29d92-103">Estructura de DOC \_ info \_ 3</span><span class="sxs-lookup"><span data-stu-id="29d92-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="29d92-104">La estructura **doc \_ info \_ 3** describe un documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="29d92-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d92-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29d92-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="29d92-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="29d92-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29d92-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="29d92-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="29d92-108">Puntero a una cadena terminada en null que especifica el nombre del documento.</span><span class="sxs-lookup"><span data-stu-id="29d92-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="29d92-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="29d92-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="29d92-110">Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="29d92-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="29d92-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="29d92-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="29d92-112">Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.</span><span class="sxs-lookup"><span data-stu-id="29d92-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="29d92-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="29d92-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="29d92-114">Marcas.</span><span class="sxs-lookup"><span data-stu-id="29d92-114">Flags.</span></span> <span data-ttu-id="29d92-115">Actualmente, puede ser **null** o el siguiente.</span><span class="sxs-lookup"><span data-stu-id="29d92-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="29d92-116">Marca</span><span class="sxs-lookup"><span data-stu-id="29d92-116">Flag</span></span>                 | <span data-ttu-id="29d92-117">Significado</span><span class="sxs-lookup"><span data-stu-id="29d92-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d92-118">escritura de DI \_ MEMORYMAP \_</span><span class="sxs-lookup"><span data-stu-id="29d92-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="29d92-119">Hace que [**StartDocPrinter**](startdocprinter.md) no use [**AddJob**](addjob.md) y [**ScheduleJob**](schedulejob.md) para la impresión local.</span><span class="sxs-lookup"><span data-stu-id="29d92-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29d92-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29d92-120">Remarks</span></span>

<span data-ttu-id="29d92-121">La \_ \_ configuración de escritura de di MEMORYMAP en la **información de documento \_ \_ 3** es una optimización.</span><span class="sxs-lookup"><span data-stu-id="29d92-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="29d92-122">Esto permite que GDI asigne los archivos de cola de impresión en la aplicación y acelere la grabación.</span><span class="sxs-lookup"><span data-stu-id="29d92-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="29d92-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d92-123">Requirements</span></span>



| <span data-ttu-id="29d92-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d92-124">Requirement</span></span> | <span data-ttu-id="29d92-125">Value</span><span class="sxs-lookup"><span data-stu-id="29d92-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d92-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d92-126">Minimum supported client</span></span><br/> | <span data-ttu-id="29d92-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="29d92-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="29d92-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d92-128">Minimum supported server</span></span><br/> | <span data-ttu-id="29d92-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29d92-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="29d92-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29d92-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d92-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29d92-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="29d92-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="29d92-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="29d92-133">**\_ Información de documento \_ \_ 3W** (Unicode) y **\_ información de documento \_ \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="29d92-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="29d92-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="29d92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d92-135">Impresión</span><span class="sxs-lookup"><span data-stu-id="29d92-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="29d92-136">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="29d92-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="29d92-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="29d92-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="29d92-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="29d92-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="29d92-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="29d92-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




