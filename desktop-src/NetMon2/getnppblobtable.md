---
description: La función GetNPPBlobTable recupera una tabla BLOB NPP que representa las NIC de registro del equipo local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Función GetNPPBlobTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910885"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="68019-103">GetNPPBlobTable función)</span><span class="sxs-lookup"><span data-stu-id="68019-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="68019-104">La función **GetNPPBlobTable** recupera una tabla BLOB NPP que representa las NIC de registro del equipo local.</span><span class="sxs-lookup"><span data-stu-id="68019-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="68019-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68019-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="68019-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68019-107">*hFilterBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68019-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68019-108">Identificador de un BLOB en filtro que limita los blobs NPP devueltos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="68019-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="68019-109">*ppBlobTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68019-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68019-110">Puntero a una estructura de [ \_ tabla de BLOB](blob-table.md) que contiene al menos un puntero de BLOB.</span><span class="sxs-lookup"><span data-stu-id="68019-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68019-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68019-111">Return value</span></span>

<span data-ttu-id="68019-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="68019-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68019-113">Si la función no es correcta, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="68019-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="68019-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68019-114">Return code</span></span>                                                                                                | <span data-ttu-id="68019-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="68019-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68019-116"><dt>**NMERR \_ no \_ hay \_ dll NPP**</dt></span><span class="sxs-lookup"><span data-stu-id="68019-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="68019-117">No se encontró ningún dll en el directorio NPP.</span><span class="sxs-lookup"><span data-stu-id="68019-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="68019-118"><dt>**NMERR \_ no hay ningún \_ \_ dll NPP válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68019-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="68019-119">Ninguno de los archivos DLL del directorio NPP eran archivos dll NPP válidos.</span><span class="sxs-lookup"><span data-stu-id="68019-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="68019-120"><dt>**NMERR \_ no \_ \_ NPPS coincidente**</dt></span><span class="sxs-lookup"><span data-stu-id="68019-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="68019-121">Se detectaron blobs NPP, pero ninguno pasó la prueba de filtro.</span><span class="sxs-lookup"><span data-stu-id="68019-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="68019-122"><dt>**NMERR \_ fuera \_ del \_ memorando**</dt></span><span class="sxs-lookup"><span data-stu-id="68019-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="68019-123">Monitor de red no pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="68019-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="68019-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68019-124">Remarks</span></span>

<span data-ttu-id="68019-125">El BLOB denominado por *hFilterBlob* también puede ser un BLOB especial.</span><span class="sxs-lookup"><span data-stu-id="68019-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="68019-126">Si establece la marca en el BLOB de filtro en **true**, la tabla BLOB devuelta también puede incluir blobs especiales.</span><span class="sxs-lookup"><span data-stu-id="68019-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="68019-127">Si el BLOB llamado por *hFilterBlob* es un BLOB especial, la interfaz de usuario de monitor de red intentará procesarlo.</span><span class="sxs-lookup"><span data-stu-id="68019-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="68019-128">Por ejemplo, supongamos que una llamada anterior devuelve un BLOB especial del NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="68019-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="68019-129">La aplicación inserta la etiqueta necesaria, el nombre de la máquina \_ .</span><span class="sxs-lookup"><span data-stu-id="68019-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="68019-130">A continuación, el buscador pasa este BLOB al NPP remoto, que luego devuelve una tabla de los blobs NPP asociados al nombre de la máquina.</span><span class="sxs-lookup"><span data-stu-id="68019-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="68019-131">Para destruir todos los blobs devueltos y la tabla BLOB, el autor de la llamada es responsable de llamar a la función **DestroyBlob** .</span><span class="sxs-lookup"><span data-stu-id="68019-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68019-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68019-132">Requirements</span></span>



| <span data-ttu-id="68019-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="68019-133">Requirement</span></span> | <span data-ttu-id="68019-134">Value</span><span class="sxs-lookup"><span data-stu-id="68019-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68019-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68019-135">Minimum supported client</span></span><br/> | <span data-ttu-id="68019-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68019-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68019-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68019-137">Minimum supported server</span></span><br/> | <span data-ttu-id="68019-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68019-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68019-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68019-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="68019-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68019-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="68019-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68019-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="68019-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68019-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="68019-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68019-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68019-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68019-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




