---
description: La \_ estructura doc info \_ 2 describe un documento que se va a imprimir.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Estructura de DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697514"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="b5d73-103">Estructura de DOC \_ info \_ 2</span><span class="sxs-lookup"><span data-stu-id="b5d73-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="b5d73-104">La estructura **doc \_ info \_ 2** describe un documento que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="b5d73-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5d73-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="b5d73-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5d73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5d73-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="b5d73-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="b5d73-108">Puntero a una cadena terminada en null que especifica el nombre del documento.</span><span class="sxs-lookup"><span data-stu-id="b5d73-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="b5d73-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="b5d73-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="b5d73-110">Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="b5d73-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="b5d73-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="b5d73-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="b5d73-112">Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.</span><span class="sxs-lookup"><span data-stu-id="b5d73-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="b5d73-113">**dwMode**</span><span class="sxs-lookup"><span data-stu-id="b5d73-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="b5d73-114">Informa al administrador de trabajos de impresión de la naturaleza de los datos que deben seguir.</span><span class="sxs-lookup"><span data-stu-id="b5d73-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="b5d73-115">Si este valor es cero, el administrador de trabajos de impresión trata los datos enviados por las llamadas subsiguientes a [**WritePrinter**](writeprinter.md) como un trabajo de impresión normal (tanto si se ha puesto en cola como si no depende de la propiedad de impresora).</span><span class="sxs-lookup"><span data-stu-id="b5d73-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="b5d73-116">Si este valor es DI \_ Channel, solo se abre un canal de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="b5d73-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="b5d73-117">En este caso, los datos pasados a las llamadas subsiguientes a **WritePrinter** se envían a la impresora o las llamadas posteriores a [**ReadPrinter**](readprinter.md) recuperan datos de la impresora.</span><span class="sxs-lookup"><span data-stu-id="b5d73-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="b5d73-118">Este modo se mantiene efectivo hasta que se llama a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .</span><span class="sxs-lookup"><span data-stu-id="b5d73-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="b5d73-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="b5d73-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="b5d73-120">Reservado para uso interno; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b5d73-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5d73-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5d73-121">Requirements</span></span>



| <span data-ttu-id="b5d73-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d73-122">Requirement</span></span> | <span data-ttu-id="b5d73-123">Value</span><span class="sxs-lookup"><span data-stu-id="b5d73-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d73-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5d73-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d73-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5d73-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b5d73-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5d73-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d73-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5d73-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b5d73-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5d73-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5d73-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5d73-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b5d73-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b5d73-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5d73-131">**\_ Información de documento \_ \_ 2W** (Unicode) y **\_ información de documento \_ \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5d73-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="b5d73-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5d73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d73-133">Impresión</span><span class="sxs-lookup"><span data-stu-id="b5d73-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b5d73-134">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b5d73-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b5d73-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="b5d73-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="b5d73-136">**ReadPrinter**</span><span class="sxs-lookup"><span data-stu-id="b5d73-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="b5d73-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b5d73-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="b5d73-138">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="b5d73-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




