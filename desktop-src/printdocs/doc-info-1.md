---
description: La \_ estructura doc info \_ 1 describe un documento que se va a imprimir.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Estructura de DOC_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276666"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="89a3e-103">Estructura de información de documento \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="89a3e-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="89a3e-104">La estructura **doc \_ info \_ 1** describe un documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="89a3e-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a3e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89a3e-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="89a3e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="89a3e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="89a3e-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="89a3e-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="89a3e-108">Puntero a una cadena terminada en null que especifica el nombre del documento.</span><span class="sxs-lookup"><span data-stu-id="89a3e-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="89a3e-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="89a3e-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="89a3e-110">Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="89a3e-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="89a3e-111">Para imprimir en una impresora, establezca este **valor en NULL**.</span><span class="sxs-lookup"><span data-stu-id="89a3e-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="89a3e-112">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="89a3e-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="89a3e-113">Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.</span><span class="sxs-lookup"><span data-stu-id="89a3e-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89a3e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89a3e-114">Requirements</span></span>



| <span data-ttu-id="89a3e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a3e-115">Requirement</span></span> | <span data-ttu-id="89a3e-116">Value</span><span class="sxs-lookup"><span data-stu-id="89a3e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a3e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89a3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89a3e-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="89a3e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89a3e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89a3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89a3e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="89a3e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89a3e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89a3e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89a3e-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89a3e-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="89a3e-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="89a3e-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89a3e-124">**\_ Información de documento \_ \_ 1W** (Unicode) y **\_ información de documento \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="89a3e-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="89a3e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="89a3e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a3e-126">Impresión</span><span class="sxs-lookup"><span data-stu-id="89a3e-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="89a3e-127">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="89a3e-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="89a3e-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="89a3e-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




