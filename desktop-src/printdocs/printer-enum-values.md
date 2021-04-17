---
description: La \_ estructura de valores enum de impresora \_ especifica el nombre del valor, el tipo y los datos para un valor de configuración de impresora devuelto por la función EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Estructura de PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716336"
---
# <a name="printer_enum_values-structure"></a><span data-ttu-id="dc06d-103">\_Estructura de valores de enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="dc06d-103">PRINTER\_ENUM\_VALUES structure</span></span>

<span data-ttu-id="dc06d-104">La estructura de **\_ \_ valores enum de impresora** especifica el nombre del valor, el tipo y los datos para un valor de configuración de impresora devuelto por la función [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="dc06d-104">The **PRINTER\_ENUM\_VALUES** structure specifies the value name, type, and data for a printer configuration value returned by the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc06d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc06d-105">Syntax</span></span>


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a><span data-ttu-id="dc06d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc06d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc06d-107">**pValueName**</span><span class="sxs-lookup"><span data-stu-id="dc06d-107">**pValueName**</span></span>
</dt> <dd>

<span data-ttu-id="dc06d-108">Puntero a una cadena terminada en null que especifica el nombre del valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="dc06d-108">Pointer to a null-terminated string that specifies the name of the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="dc06d-109">**cbValueName**</span><span class="sxs-lookup"><span data-stu-id="dc06d-109">**cbValueName**</span></span>
</dt> <dd>

<span data-ttu-id="dc06d-110">El número de bytes en el miembro **pValueName** , incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dc06d-110">The number of bytes in the **pValueName** member, including the terminating NULL character.</span></span>

</dd> <dt>

<span data-ttu-id="dc06d-111">**dwType**</span><span class="sxs-lookup"><span data-stu-id="dc06d-111">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="dc06d-112">Código que indica el tipo de datos al que apunta el miembro **pdata** .</span><span class="sxs-lookup"><span data-stu-id="dc06d-112">A code indicating the type of data pointed to by the **pData** member.</span></span> <span data-ttu-id="dc06d-113">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="dc06d-113">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="dc06d-114">**pData**</span><span class="sxs-lookup"><span data-stu-id="dc06d-114">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="dc06d-115">Puntero a un búfer que contiene los datos para el valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="dc06d-115">Pointer to a buffer containing the data for the retrieved value.</span></span>

</dd> <dt>

<span data-ttu-id="dc06d-116">**cbData**</span><span class="sxs-lookup"><span data-stu-id="dc06d-116">**cbData**</span></span>
</dt> <dd>

<span data-ttu-id="dc06d-117">Número de bytes recuperados en el búfer de **pdata** .</span><span class="sxs-lookup"><span data-stu-id="dc06d-117">The number of bytes retrieved in the **pData** buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc06d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc06d-118">Requirements</span></span>



| <span data-ttu-id="dc06d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc06d-119">Requirement</span></span> | <span data-ttu-id="dc06d-120">Value</span><span class="sxs-lookup"><span data-stu-id="dc06d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc06d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc06d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc06d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dc06d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dc06d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc06d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc06d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc06d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dc06d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc06d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc06d-126"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc06d-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dc06d-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="dc06d-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dc06d-128">**\_ \_ Enumeración \_ de impresora VALUESW** (Unicode) y **\_ \_ \_ valores de enumeración de impresora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dc06d-128">**\_PRINTER\_ENUM\_VALUESW** (Unicode) and **\_PRINTER\_ENUM\_VALUESA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="dc06d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc06d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc06d-130">Impresión</span><span class="sxs-lookup"><span data-stu-id="dc06d-130">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dc06d-131">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="dc06d-131">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="dc06d-132">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="dc06d-132">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> </dl>

 

