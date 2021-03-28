---
description: Estos tipos de datos se pueden utilizar para especificar el tipo de un valor del registro.
title: Tipos de datos del registro (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998983"
---
# <a name="registry-data-types"></a><span data-ttu-id="e31e7-103">Tipos de datos del registro</span><span class="sxs-lookup"><span data-stu-id="e31e7-103">Registry Data Types</span></span>

<span data-ttu-id="e31e7-104">Estos tipos de datos se pueden utilizar para especificar el tipo de un valor del registro.</span><span class="sxs-lookup"><span data-stu-id="e31e7-104">These data types can be used to specify the type of a registry value.</span></span>



| <span data-ttu-id="e31e7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e31e7-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="e31e7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e31e7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <span data-ttu-id="e31e7-107"><dt>**\_binario de reg**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-107"><dt>**REG\_BINARY**</dt></span></span> </dl>                                          | <span data-ttu-id="e31e7-108">Datos binarios en cualquier formato.</span><span class="sxs-lookup"><span data-stu-id="e31e7-108">Binary data in any form.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <span data-ttu-id="e31e7-109"><dt>**\_valor DWORD reg**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-109"><dt>**REG\_DWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="e31e7-110">número de bits 32.</span><span class="sxs-lookup"><span data-stu-id="e31e7-110">32-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <span data-ttu-id="e31e7-111"><dt>**QWord de REG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-111"><dt>**REG\_QWORD**</dt></span></span> </dl>                                             | <span data-ttu-id="e31e7-112">número de bits 64.</span><span class="sxs-lookup"><span data-stu-id="e31e7-112">64-bit number.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <span data-ttu-id="e31e7-113"><dt>**REG \_ DWORD \_ Little \_ endian**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-113"><dt>**REG\_DWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="e31e7-114">32: número de bits en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="e31e7-114">32-bit number in little-endian format.</span></span> <span data-ttu-id="e31e7-115">Es equivalente a **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="e31e7-115">This is equivalent to **REG\_DWORD**.</span></span><br/> <span data-ttu-id="e31e7-116">En el formato Little-endian, se almacena un valor multibyte en la memoria desde el byte más bajo (el "pequeño extremo") hasta el byte más alto.</span><span class="sxs-lookup"><span data-stu-id="e31e7-116">In little-endian format, a multibyte value is stored in memory from the lowest byte (the "little end") to the highest byte.</span></span> <span data-ttu-id="e31e7-117">Por ejemplo, el valor 0x12345678 se almacena como (0x78 0x56 0x34 0X12) en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="e31e7-117">For example, the value 0x12345678 is stored as (0x78 0x56 0x34 0x12) in little-endian format.</span></span><br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <span data-ttu-id="e31e7-118"><dt>**REG \_ QWord \_ Little \_ endian**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-118"><dt>**REG\_QWORD\_LITTLE\_ENDIAN**</dt></span></span> </dl> | <span data-ttu-id="e31e7-119">Número de 64 bits en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="e31e7-119">A 64-bit number in little-endian format.</span></span> <span data-ttu-id="e31e7-120">Esto es equivalente a **reg \_ QWord**.</span><span class="sxs-lookup"><span data-stu-id="e31e7-120">This is equivalent to **REG\_QWORD**.</span></span> <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <span data-ttu-id="e31e7-121"><dt>**REG \_ DWORD \_ Big \_ endian**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-121"><dt>**REG\_DWORD\_BIG\_ENDIAN**</dt></span></span> </dl>          | <span data-ttu-id="e31e7-122">32: número de bits en formato Big-Endian.</span><span class="sxs-lookup"><span data-stu-id="e31e7-122">32-bit number in big-endian format.</span></span><br/> <span data-ttu-id="e31e7-123">En el formato Big-endian, se almacena un valor multibyte en la memoria desde el byte más alto (el "Big end") hasta el byte más bajo.</span><span class="sxs-lookup"><span data-stu-id="e31e7-123">In big-endian format, a multibyte value is stored in memory from the highest byte (the "big end") to the lowest byte.</span></span> <span data-ttu-id="e31e7-124">Por ejemplo, el valor 0x12345678 se almacena como (0X12 0x34 0x56 0x78) en formato Big-Endian.</span><span class="sxs-lookup"><span data-stu-id="e31e7-124">For example, the value 0x12345678 is stored as (0x12 0x34 0x56 0x78) in big-endian format.</span></span><br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <span data-ttu-id="e31e7-125"><dt>**REG \_ expandir \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-125"><dt>**REG\_EXPAND\_SZ**</dt></span></span> </dl>                                | <span data-ttu-id="e31e7-126">Cadena terminada en null que contiene referencias no expandidas a variables de entorno (por ejemplo, "% PATH%").</span><span class="sxs-lookup"><span data-stu-id="e31e7-126">Null-terminated string that contains unexpanded references to environment variables (for example, "%PATH%").</span></span> <span data-ttu-id="e31e7-127">Será una cadena ANSI o Unicode, en función de si se utilizan las funciones Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="e31e7-127">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <span data-ttu-id="e31e7-128"><dt>**\_vínculo reg**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-128"><dt>**REG\_LINK**</dt></span></span> </dl>                                                | <span data-ttu-id="e31e7-129">Vínculo simbólico Unicode.</span><span class="sxs-lookup"><span data-stu-id="e31e7-129">Unicode symbolic link.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <span data-ttu-id="e31e7-130"><dt>**REG \_ multi \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-130"><dt>**REG\_MULTI\_SZ**</dt></span></span> </dl>                                   | <span data-ttu-id="e31e7-131">Matriz de cadenas terminadas en null que finalizan con dos caracteres null.</span><span class="sxs-lookup"><span data-stu-id="e31e7-131">Array of null-terminated strings that are terminated by two null characters.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <span data-ttu-id="e31e7-132"><dt>**REG \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-132"><dt>**REG\_NONE**</dt></span></span> </dl>                                                | <span data-ttu-id="e31e7-133">No hay ningún tipo de valor definido.</span><span class="sxs-lookup"><span data-stu-id="e31e7-133">No defined value type.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <span data-ttu-id="e31e7-134"><dt>**\_lista de recursos del registro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-134"><dt>**REG\_RESOURCE\_LIST**</dt></span></span> </dl>                    | <span data-ttu-id="e31e7-135">Lista de recursos de controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e31e7-135">Device-driver resource list.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <span data-ttu-id="e31e7-136"><dt>**Registro \_ SZ**</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-136"><dt>**REG\_SZ**</dt></span></span> </dl>                                                      | <span data-ttu-id="e31e7-137">Cadena terminada en un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="e31e7-137">Null-terminated string.</span></span> <span data-ttu-id="e31e7-138">Será una cadena ANSI o Unicode, en función de si se utilizan las funciones Unicode o ANSI.</span><span class="sxs-lookup"><span data-stu-id="e31e7-138">It will be a Unicode or ANSI string, depending on whether you use the Unicode or ANSI functions.</span></span><br/>                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="e31e7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e31e7-139">Requirements</span></span>



| <span data-ttu-id="e31e7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31e7-140">Requirement</span></span> | <span data-ttu-id="e31e7-141">Value</span><span class="sxs-lookup"><span data-stu-id="e31e7-141">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e31e7-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e31e7-142">Header</span></span><br/> | <dl> <span data-ttu-id="e31e7-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e31e7-143"><dt>Winnt.h</dt></span></span> </dl> |



 

 




