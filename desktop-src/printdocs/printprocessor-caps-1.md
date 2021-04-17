---
description: La \_ estructura PRINTPROCESSOR caps \_ 1 es el formato de la información de funcionalidad de la impresora que devuelve la función GetPrinterData en el búfer especificado por la variable pdata.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Estructura de PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697512"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="ef9ff-103">\_Estructura PRINTPROCESSOR Cap \_ 1</span><span class="sxs-lookup"><span data-stu-id="ef9ff-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="ef9ff-104">La estructura **PRINTPROCESSOR \_ caps \_ 1** es el formato de la información de funcionalidad de la impresora que devuelve la función [**GetPrinterData**](getprinterdata.md) en el búfer especificado por la variable *pdata* .</span><span class="sxs-lookup"><span data-stu-id="ef9ff-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef9ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef9ff-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="ef9ff-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef9ff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef9ff-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="ef9ff-108">Número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-108">The structure's version number.</span></span> <span data-ttu-id="ef9ff-109">Este valor debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="ef9ff-110">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="ef9ff-111">Máscara de bits que representa los diversos números de páginas del documento que la impresora puede imprimir en una página física.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="ef9ff-112">El bit menos significativo representa 1 página de documento por página, el siguiente bit representa 2 páginas de documento por página, etc.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="ef9ff-113">Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por página física.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="ef9ff-114">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ef9ff-115">El orden en que se imprimirán las páginas.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-115">The order in which pages will be printed.</span></span> <span data-ttu-id="ef9ff-116">Este valor puede ser \_ impresión normal, impresión inversa \_ o folleto \_ impreso.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="ef9ff-117">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="ef9ff-118">Número máximo de copias que la impresora puede controlar.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef9ff-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef9ff-119">Remarks</span></span>

<span data-ttu-id="ef9ff-120">Los valores de todos los miembros de la estructura se proporcionan mediante la función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , que se documenta en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="ef9ff-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="ef9ff-121">El administrador de trabajos de impresión llama a la función [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) de un procesador de impresión cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), especificando un nombre de valor con un formato de PrintProcCaps \_ *DataType*, donde *DataType* es el nombre de un tipo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef9ff-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef9ff-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef9ff-122">Requirements</span></span>



| <span data-ttu-id="ef9ff-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef9ff-123">Requirement</span></span> | <span data-ttu-id="ef9ff-124">Value</span><span class="sxs-lookup"><span data-stu-id="ef9ff-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9ff-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef9ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef9ff-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef9ff-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ef9ff-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef9ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef9ff-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef9ff-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ef9ff-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef9ff-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef9ff-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef9ff-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef9ff-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef9ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9ff-132">Impresión</span><span class="sxs-lookup"><span data-stu-id="ef9ff-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ef9ff-133">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ef9ff-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ef9ff-134">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="ef9ff-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

