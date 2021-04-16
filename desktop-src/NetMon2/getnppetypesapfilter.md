---
description: La función GetNPPEtypeSapFilter recupera el filtro ETYPE/SAP de un BLOB determinado.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Función GetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678582"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="02790-103">GetNPPEtypeSapFilter función)</span><span class="sxs-lookup"><span data-stu-id="02790-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="02790-104">La función **GetNPPEtypeSapFilter** recupera el filtro ETYPE/SAP de un BLOB determinado.</span><span class="sxs-lookup"><span data-stu-id="02790-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="02790-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02790-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="02790-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02790-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="02790-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="02790-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="02790-109">*pnSaps* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-110">Puntero al número de protocolos devuelto en la tabla de SAP.</span><span class="sxs-lookup"><span data-stu-id="02790-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="02790-111">*pnEtypes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-112">Puntero al número de ETYPE devuelto en la tabla ETYPE.</span><span class="sxs-lookup"><span data-stu-id="02790-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="02790-113">*ppSapTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-114">Puntero a la tabla de SAP devuelta.</span><span class="sxs-lookup"><span data-stu-id="02790-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="02790-115">*ppEtypeTable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-116">Puntero a la tabla ETYPE devuelta.</span><span class="sxs-lookup"><span data-stu-id="02790-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="02790-117">*pFilterFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-118">Puntero a las marcas de filtro devueltas.</span><span class="sxs-lookup"><span data-stu-id="02790-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="02790-119">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="02790-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02790-120">Identificador de un BLOB de error, que especifica la ubicación en el BLOB original donde se produjo el error (si existe).</span><span class="sxs-lookup"><span data-stu-id="02790-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02790-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02790-121">Return value</span></span>

<span data-ttu-id="02790-122">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="02790-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="02790-123">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="02790-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="02790-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02790-124">Remarks</span></span>

<span data-ttu-id="02790-125">La información de ETYPE/SAP se almacena en la categoría **configuración** de la sección de **propietario** NPP.</span><span class="sxs-lookup"><span data-stu-id="02790-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="02790-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02790-126">Requirements</span></span>



| <span data-ttu-id="02790-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="02790-127">Requirement</span></span> | <span data-ttu-id="02790-128">Value</span><span class="sxs-lookup"><span data-stu-id="02790-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02790-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02790-129">Minimum supported client</span></span><br/> | <span data-ttu-id="02790-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="02790-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02790-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02790-131">Minimum supported server</span></span><br/> | <span data-ttu-id="02790-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="02790-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02790-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02790-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="02790-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="02790-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="02790-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02790-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="02790-136"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02790-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="02790-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02790-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02790-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02790-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02790-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="02790-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02790-140">SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="02790-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




