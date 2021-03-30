---
description: Recupera datos de las entradas especificadas que pertenecen a una entrada EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423207"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="428e8-103">SdbQueryDataExTagID función)</span><span class="sxs-lookup"><span data-stu-id="428e8-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="428e8-104">Recupera datos de las entradas especificadas que pertenecen a una entrada EXE.</span><span class="sxs-lookup"><span data-stu-id="428e8-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="428e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="428e8-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="428e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="428e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="428e8-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="428e8-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="428e8-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="428e8-109">*tiExe* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="428e8-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-110">[**TAGID**](tagid.md) de la entrada exe.</span><span class="sxs-lookup"><span data-stu-id="428e8-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="428e8-111">*lpszDataName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="428e8-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-112">Nombre de la entrada de datos que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="428e8-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="428e8-113">Para especificar varias entradas, separe los nombres con el carácter de barra diagonal inversa (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="428e8-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="428e8-114">Si este parámetro es **null**, la función intenta devolver todas las entradas de datos.</span><span class="sxs-lookup"><span data-stu-id="428e8-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="428e8-115">*lpdwDataType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="428e8-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-116">El tipo de datos de las entradas devueltas.</span><span class="sxs-lookup"><span data-stu-id="428e8-116">The data type of the returned entries.</span></span> <span data-ttu-id="428e8-117">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="428e8-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="428e8-118">**\_binario de reg**</span><span class="sxs-lookup"><span data-stu-id="428e8-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="428e8-119">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="428e8-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="428e8-120">**REG \_ multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="428e8-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="428e8-121">**REG \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="428e8-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="428e8-122">**QWord de REG \_**</span><span class="sxs-lookup"><span data-stu-id="428e8-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="428e8-123">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="428e8-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="428e8-124">*lpBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="428e8-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-125">Búfer que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="428e8-125">The buffer that receives the data.</span></span> <span data-ttu-id="428e8-126">Si el búfer no es lo suficientemente grande como para contener los datos, se produce un error en la función y se devuelve un **error de \_ \_ búfer insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="428e8-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="428e8-127">*lpcbBufferSize* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="428e8-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-128">Tamaño del búfer de *lpBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="428e8-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="428e8-129">*ptiData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="428e8-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="428e8-130">[**TAGID**](tagid.md) de la entrada de datos.</span><span class="sxs-lookup"><span data-stu-id="428e8-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="428e8-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="428e8-131">Return value</span></span>

<span data-ttu-id="428e8-132">Esta función devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="428e8-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="428e8-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="428e8-133">Return code</span></span>                                                                                                    | <span data-ttu-id="428e8-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="428e8-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="428e8-135"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="428e8-136">Uno o varios parámetros de entrada no son correctos.</span><span class="sxs-lookup"><span data-stu-id="428e8-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="428e8-137"><dt>**ERROR \_ de \_ base de BD interna \_ dañado**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="428e8-138">No se encontraron entradas de datos para la entrada EXE.</span><span class="sxs-lookup"><span data-stu-id="428e8-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="428e8-139"><dt>**ERROR \_ de \_ búfer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="428e8-140">El búfer no es suficientemente grande para contener las entradas de datos.</span><span class="sxs-lookup"><span data-stu-id="428e8-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="428e8-141"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="428e8-142">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="428e8-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="428e8-143"><dt>**\_no \_ se encontró el error**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="428e8-144">No se encontró una entrada de datos con el nombre *lpszDataName* .</span><span class="sxs-lookup"><span data-stu-id="428e8-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="428e8-145"><dt>**ERROR \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="428e8-146">La función se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="428e8-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="428e8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="428e8-147">Requirements</span></span>



| <span data-ttu-id="428e8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="428e8-148">Requirement</span></span> | <span data-ttu-id="428e8-149">Value</span><span class="sxs-lookup"><span data-stu-id="428e8-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="428e8-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="428e8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="428e8-151">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="428e8-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="428e8-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="428e8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="428e8-153">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="428e8-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="428e8-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="428e8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="428e8-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="428e8-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




