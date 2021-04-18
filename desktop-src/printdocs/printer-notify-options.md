---
description: La estructura de opciones de notificación de impresora \_ \_ especifica opciones para un objeto de notificación de cambios que supervisa una impresora o un servidor de impresión.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Estructura de PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720574"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="9e356-103">Estructura de opciones de \_ notificación de impresora \_</span><span class="sxs-lookup"><span data-stu-id="9e356-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="9e356-104">La estructura de **\_ \_ Opciones** de notificación de impresora especifica opciones para un objeto de notificación de cambios que supervisa una impresora o un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="9e356-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e356-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e356-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="9e356-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e356-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e356-107">**Versión**</span><span class="sxs-lookup"><span data-stu-id="9e356-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="9e356-108">Versión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="9e356-108">The version of this structure.</span></span> <span data-ttu-id="9e356-109">Establezca este miembro en 2.</span><span class="sxs-lookup"><span data-stu-id="9e356-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="9e356-110">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="9e356-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9e356-111">Marca de bits.</span><span class="sxs-lookup"><span data-stu-id="9e356-111">A bit flag.</span></span> <span data-ttu-id="9e356-112">Si establece la marca de \_ \_ actualización de opciones \_ de notificación de impresora en una llamada a la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la función proporciona los datos actuales de todos los campos supervisados de información de la impresora.</span><span class="sxs-lookup"><span data-stu-id="9e356-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="9e356-113">La función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) omite el miembro **Flags** .</span><span class="sxs-lookup"><span data-stu-id="9e356-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="9e356-114">**Recuento**</span><span class="sxs-lookup"><span data-stu-id="9e356-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="9e356-115">Número de elementos de la matriz **pTypes** .</span><span class="sxs-lookup"><span data-stu-id="9e356-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="9e356-116">**pTypes**</span><span class="sxs-lookup"><span data-stu-id="9e356-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="9e356-117">Puntero a una matriz de estructuras [**de \_ \_ \_ tipo de opciones de notificación de impresora**](printer-notify-options-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9e356-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="9e356-118">Utilice un elemento de esta matriz para especificar los campos de información de la impresora que se van a supervisar y un elemento para especificar los campos de información de los trabajos que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="9e356-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="9e356-119">Puede supervisar la información de la impresora, la información del trabajo o ambas cosas.</span><span class="sxs-lookup"><span data-stu-id="9e356-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e356-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e356-120">Remarks</span></span>

<span data-ttu-id="9e356-121">Use esta estructura con la función [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar el conjunto de campos de información de la impresora o del trabajo para supervisar los cambios.</span><span class="sxs-lookup"><span data-stu-id="9e356-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="9e356-122">Use esta estructura con la función [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar los datos actuales de todos los campos supervisados de información de la impresora y del trabajo.</span><span class="sxs-lookup"><span data-stu-id="9e356-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="9e356-123">En este caso, el miembro **Flags** especifica la \_ marca de actualización opciones de notificación de impresora \_ \_ y la función omite los demás miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9e356-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e356-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e356-124">Requirements</span></span>



| <span data-ttu-id="9e356-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e356-125">Requirement</span></span> | <span data-ttu-id="9e356-126">Value</span><span class="sxs-lookup"><span data-stu-id="9e356-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e356-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e356-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9e356-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9e356-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9e356-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e356-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9e356-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e356-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9e356-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e356-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e356-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e356-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e356-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e356-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e356-134">Impresión</span><span class="sxs-lookup"><span data-stu-id="9e356-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9e356-135">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="9e356-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9e356-136">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="9e356-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="9e356-137">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="9e356-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="9e356-138">**\_tipo de \_ Opciones de notificación de impresora \_**</span><span class="sxs-lookup"><span data-stu-id="9e356-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




