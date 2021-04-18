---
description: La estructura de información de la impresora \_ \_ 1 especifica información general de la impresora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Estructura de PRINTER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720590"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="b3513-103">Estructura de la información de la impresora \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="b3513-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="b3513-104">La estructura de información de la **impresora \_ \_ 1** especifica información general de la impresora.</span><span class="sxs-lookup"><span data-stu-id="b3513-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3513-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3513-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="b3513-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3513-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3513-107">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="b3513-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b3513-108">Especifica información sobre los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="b3513-108">Specifies information about the returned data.</span></span> <span data-ttu-id="b3513-109">A continuación se muestran los valores de este miembro.</span><span class="sxs-lookup"><span data-stu-id="b3513-109">Following are the values for this member.</span></span>



| <span data-ttu-id="b3513-110">Value</span><span class="sxs-lookup"><span data-stu-id="b3513-110">Value</span></span>                    | <span data-ttu-id="b3513-111">Significado</span><span class="sxs-lookup"><span data-stu-id="b3513-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3513-112">\_expansión de enum de impresora \_</span><span class="sxs-lookup"><span data-stu-id="b3513-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="b3513-113">Un proveedor de impresión puede establecer esta marca como una sugerencia para una aplicación que llama para enumerar este objeto más allá si está habilitada la expansión predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b3513-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="b3513-114">Por ejemplo, cuando se enumeran los dominios, un proveedor de impresión puede indicar el dominio del usuario mediante el establecimiento de esta marca.</span><span class="sxs-lookup"><span data-stu-id="b3513-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="b3513-115">\_contenedor de enum de impresora \_</span><span class="sxs-lookup"><span data-stu-id="b3513-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="b3513-116">Si se establece esta marca, el objeto de impresora puede contener objetos enumerables.</span><span class="sxs-lookup"><span data-stu-id="b3513-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="b3513-117">Por ejemplo, el objeto puede ser un servidor de impresión que contiene impresoras.</span><span class="sxs-lookup"><span data-stu-id="b3513-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="b3513-118">\_Enumeración de impresora \_ ICON1</span><span class="sxs-lookup"><span data-stu-id="b3513-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="b3513-119">Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un nombre de red de nivel superior, como la red de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b3513-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="b3513-120">\_Enumeración de impresora \_ ICON2</span><span class="sxs-lookup"><span data-stu-id="b3513-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="b3513-121">Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un dominio de red.</span><span class="sxs-lookup"><span data-stu-id="b3513-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="b3513-122">\_Enumeración de impresora \_ ICON3</span><span class="sxs-lookup"><span data-stu-id="b3513-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="b3513-123">Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="b3513-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="b3513-124">\_Enumeración de impresora \_ ICON4</span><span class="sxs-lookup"><span data-stu-id="b3513-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="b3513-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b3513-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b3513-126">\_Enumeración de impresora \_ ICON5</span><span class="sxs-lookup"><span data-stu-id="b3513-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="b3513-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b3513-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b3513-128">\_Enumeración de impresora \_ ICON6</span><span class="sxs-lookup"><span data-stu-id="b3513-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="b3513-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b3513-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b3513-130">\_Enumeración de impresora \_ ICON7</span><span class="sxs-lookup"><span data-stu-id="b3513-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="b3513-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b3513-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b3513-132">\_Enumeración de impresora \_ ICON8</span><span class="sxs-lookup"><span data-stu-id="b3513-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="b3513-133">Indica que, cuando sea necesario, una aplicación debe mostrar un icono que identifique el objeto como una impresora.</span><span class="sxs-lookup"><span data-stu-id="b3513-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="b3513-134">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="b3513-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="b3513-135">Puntero a una cadena terminada en null que describe el contenido de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b3513-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3513-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="b3513-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="b3513-137">Puntero a una cadena terminada en null que nombra el contenido de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b3513-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3513-138">**pComment**</span><span class="sxs-lookup"><span data-stu-id="b3513-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="b3513-139">Puntero a una cadena terminada en null que contiene datos adicionales que describen la estructura.</span><span class="sxs-lookup"><span data-stu-id="b3513-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3513-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3513-140">Requirements</span></span>



| <span data-ttu-id="b3513-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3513-141">Requirement</span></span> | <span data-ttu-id="b3513-142">Value</span><span class="sxs-lookup"><span data-stu-id="b3513-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3513-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3513-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b3513-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b3513-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b3513-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3513-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b3513-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3513-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b3513-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3513-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3513-148"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3513-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b3513-149">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b3513-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b3513-150">Información de la **\_ impresora \_ \_ 1W** (Unicode) e información de la **\_ impresora \_ \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b3513-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="b3513-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3513-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3513-152">Impresión</span><span class="sxs-lookup"><span data-stu-id="b3513-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b3513-153">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b3513-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b3513-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="b3513-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="b3513-155">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="b3513-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="b3513-156">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b3513-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="b3513-157">**Información de la impresora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="b3513-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="b3513-158">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b3513-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




