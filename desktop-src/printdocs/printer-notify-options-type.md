---
description: La \_ \_ \_ estructura de tipo de opciones de notificación de impresora especifica el conjunto de campos de información de la impresora o del trabajo que va a supervisar un objeto de notificación de cambio de impresora. Una llamada a la función FindFirstPrinterChangeNotification especifica una \_ \_ estructura de opciones de notificación de impresora, que contiene una matriz de \_ estructuras de tipo opciones de notificación de impresora \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Estructura de PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716253"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="6e4a5-103">\_Estructura de \_ tipo de opciones de notificación de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6e4a5-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="6e4a5-104">La estructura de tipo de opciones de notificación de impresora especifica el conjunto de campos de información de la impresora o del trabajo que va a supervisar un objeto de notificación de cambio de impresora. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="6e4a5-105">Una llamada a la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) especifica una estructura de [**\_ \_ Opciones de notificación de impresora**](printer-notify-options.md) , que contiene una matriz de estructuras de **\_ \_ \_ tipo opciones de notificación de impresora** .</span><span class="sxs-lookup"><span data-stu-id="6e4a5-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4a5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e4a5-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="6e4a5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e4a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e4a5-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-109">Tipo que se va a inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-109">The type to be watched.</span></span> <span data-ttu-id="6e4a5-110">Este miembro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="6e4a5-111">Value</span><span class="sxs-lookup"><span data-stu-id="6e4a5-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="6e4a5-112">Significado</span><span class="sxs-lookup"><span data-stu-id="6e4a5-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="6e4a5-113"><dt>**Trabajo \_ de NOTIFICAr \_ tipo**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="6e4a5-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="6e4a5-114">Indica que los campos especificados en la matriz **pFields** son \_ constantes de campo de notificación de trabajo \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="6e4a5-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="6e4a5-115"><dt>**Impresora \_ de NOTIFICAr el \_ tipo**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="6e4a5-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="6e4a5-116">Indica que los campos especificados en la matriz **pFields** son \_ constantes de campo de notificación de impresora \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="6e4a5-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e4a5-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e4a5-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-120">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e4a5-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="6e4a5-123">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-124">Número de elementos de la matriz **pFields** .</span><span class="sxs-lookup"><span data-stu-id="6e4a5-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="6e4a5-125">**pFields**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="6e4a5-126">Puntero a una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-126">A pointer to an array of values.</span></span> <span data-ttu-id="6e4a5-127">Cada elemento de la matriz especifica un campo de información de trabajo o impresora de interés.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="6e4a5-128">Para obtener una lista de los campos de información de la impresora y el trabajo admitidos, consulte la estructura de [**\_ \_ \_ datos de notificación**](printer-notify-info-data.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="6e4a5-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e4a5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e4a5-129">Requirements</span></span>



| <span data-ttu-id="6e4a5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e4a5-130">Requirement</span></span> | <span data-ttu-id="6e4a5-131">Value</span><span class="sxs-lookup"><span data-stu-id="6e4a5-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4a5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e4a5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4a5-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e4a5-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6e4a5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e4a5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4a5-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e4a5-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6e4a5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e4a5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e4a5-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e4a5-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e4a5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e4a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4a5-139">Impresión</span><span class="sxs-lookup"><span data-stu-id="6e4a5-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6e4a5-140">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="6e4a5-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="6e4a5-141">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="6e4a5-142">**\_datos de \_ información de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="6e4a5-143">**\_Opciones de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="6e4a5-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




