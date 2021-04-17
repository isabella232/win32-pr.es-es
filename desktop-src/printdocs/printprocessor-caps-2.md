---
description: Representa la información de funcionalidad de la impresora.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Estructura de PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697497"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="2e6ac-103">Estructura de PRINTPROCESSOR \_ Cap \_ 2</span><span class="sxs-lookup"><span data-stu-id="2e6ac-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="2e6ac-104">Representa la información de funcionalidad de la impresora.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e6ac-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="2e6ac-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e6ac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e6ac-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-108">Valor que indica el número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ac-109">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-110">Máscara de bits que representa los diversos números de páginas del documento que la impresora puede imprimir en un lado único de una hoja física.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="2e6ac-111">El bit menos significativo representa una página de documento por lado, el siguiente bit representa 2 páginas de documento por lado, etc.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="2e6ac-112">Por ejemplo, 0x0000810B indica que la impresora admite 1, 2, 4, 9 y 16 páginas de documento por lado físico.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ac-113">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-114">Un valor de marca que indica el orden en el que se imprimirán las páginas.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="2e6ac-115">Puede ser impresión **normal \_**, impresión **inversa \_** o **folleto \_ impreso**.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ac-116">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-117">Número máximo de copias que la impresora puede controlar.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ac-118">**dwNupDirectionCaps**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-119">Los patrones disponibles cuando se imprimen varias páginas del documento en el mismo lado de una hoja de papel.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="2e6ac-120">Las posibles marcas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e6ac-120">The possible flags are the following:</span></span>



| <span data-ttu-id="2e6ac-121">Value</span><span class="sxs-lookup"><span data-stu-id="2e6ac-121">Value</span></span>                     | <span data-ttu-id="2e6ac-122">Significado</span><span class="sxs-lookup"><span data-stu-id="2e6ac-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6ac-123">PPCAPS \_ a la derecha \_ \_</span><span class="sxs-lookup"><span data-stu-id="2e6ac-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="2e6ac-124">Las páginas aparecen en filas de derecha a izquierda, cada fila subsiguiente debajo de su predecesor.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="2e6ac-125">PPCAPS \_ \_ a la \_ derecha</span><span class="sxs-lookup"><span data-stu-id="2e6ac-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="2e6ac-126">Las páginas aparecen en columnas de arriba abajo, cada columna subsiguiente a la derecha de su predecesora.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="2e6ac-127">PPCAPS \_ a la izquierda \_ \_</span><span class="sxs-lookup"><span data-stu-id="2e6ac-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="2e6ac-128">Las páginas aparecen en filas de izquierda a derecha, cada fila subsiguiente debajo de su predecesor.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="2e6ac-129">PPCAPS \_ \_ a la \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="2e6ac-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="2e6ac-130">Las páginas aparecen en columnas de arriba abajo, cada columna subsiguiente a la izquierda de su predecesora.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2e6ac-131">**dwNupBorderCaps**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-132">Solo puede ser PPCAPS \_ Border \_ Print, lo que indica que, cuando se imprimen varias páginas del documento en una sola cara de una hoja física, se puede indicar a la impresora si se imprime o no un borde alrededor del área de impresión de cada página del documento.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="2e6ac-133">**dwBookletHandlingCaps**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-134">Solo puede ser PPCAPS \_ \_ , lo que indica que la impresora puede imprimir el estilo de folleto.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="2e6ac-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="2e6ac-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="2e6ac-136">Value</span><span class="sxs-lookup"><span data-stu-id="2e6ac-136">Value</span></span>                                         | <span data-ttu-id="2e6ac-137">Significado</span><span class="sxs-lookup"><span data-stu-id="2e6ac-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6ac-138">PPCAPS \_ páginas inversas \_ \_ para \_ dúplex inverso \_</span><span class="sxs-lookup"><span data-stu-id="2e6ac-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="2e6ac-139">Al imprimir en orden inverso y dúplex, el procesador puede imprimir el orden de cada par de páginas, por lo que en lugar de imprimir en el orden 4, 3, 2, 1, se imprimirán en el orden 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="2e6ac-140">PPCAPS \_ no \_ enviar \_ \_ páginas adicionales \_ para \_ dúplex</span><span class="sxs-lookup"><span data-stu-id="2e6ac-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="2e6ac-141">Al usar el dúplex, se puede indicar al procesador de impresión que no envíe una página adicional cuando hay un número impar de páginas del documento.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="2e6ac-142">El procesador respetará el valor de la mejor forma posible, pero en los casos en los que evitar una página en blanco adicional causaría una salida incorrecta, es posible que se sigan enviando las páginas adicionales.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2e6ac-143">**dwScalingCaps**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="2e6ac-144">Solo se puede \_ \_ escalar PPCAPS cuadrado, lo que indica que la impresora puede escalar la imagen de la página.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e6ac-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e6ac-145">Remarks</span></span>

<span data-ttu-id="2e6ac-146">Los valores de todos los miembros de la estructura se proporcionan mediante la función **GetPrintProcessorCapabilities** , que se documenta en el kit de controladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="2e6ac-147">Cuando una aplicación llama a [**GetPrinterData**](getprinterdata.md), el administrador de trabajos de impresión llama a la función **GetPrintProcessorCapabilities** de un procesador de impresión y especifica un nombre de valor que tiene un formato de **\_ PrintProcCaps**_DataType_, donde *DataType* es el nombre de un tipo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e6ac-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6ac-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e6ac-148">Requirements</span></span>



| <span data-ttu-id="2e6ac-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6ac-149">Requirement</span></span> | <span data-ttu-id="2e6ac-150">Value</span><span class="sxs-lookup"><span data-stu-id="2e6ac-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6ac-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6ac-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6ac-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e6ac-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2e6ac-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6ac-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6ac-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e6ac-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e6ac-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e6ac-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6ac-156"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e6ac-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e6ac-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e6ac-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6ac-158">Impresión</span><span class="sxs-lookup"><span data-stu-id="2e6ac-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2e6ac-159">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="2e6ac-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2e6ac-160">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="2e6ac-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




