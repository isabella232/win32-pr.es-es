---
description: Establece el filtro del BLOB ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Función SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360591"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="b2121-103">SetNPPEtypeSapFilter función)</span><span class="sxs-lookup"><span data-stu-id="b2121-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="b2121-104">La función **SetNPPEtypeSapFilter** establece el filtro del BLOB ETYPE/SAP.</span><span class="sxs-lookup"><span data-stu-id="b2121-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2121-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2121-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b2121-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2121-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2121-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="b2121-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-109">*nSaps* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-110">Número de SAP.</span><span class="sxs-lookup"><span data-stu-id="b2121-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-111">*nEtypes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-112">El número de ETYPE en la tabla ETYPE que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b2121-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-113">*lpSapTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-114">Un puntero a la tabla de SAP que se establece.</span><span class="sxs-lookup"><span data-stu-id="b2121-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-115">*lpEtypeTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-116">Puntero a la tabla ETYPE que se establece.</span><span class="sxs-lookup"><span data-stu-id="b2121-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-117">*FilterFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2121-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-118">Marcas de filtro que se establecen.</span><span class="sxs-lookup"><span data-stu-id="b2121-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="b2121-119">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2121-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2121-120">Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.</span><span class="sxs-lookup"><span data-stu-id="b2121-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2121-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2121-121">Return value</span></span>

<span data-ttu-id="b2121-122">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b2121-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b2121-123">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="b2121-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2121-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2121-124">Requirements</span></span>



| <span data-ttu-id="b2121-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2121-125">Requirement</span></span> | <span data-ttu-id="b2121-126">Value</span><span class="sxs-lookup"><span data-stu-id="b2121-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2121-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2121-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2121-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b2121-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2121-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2121-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2121-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2121-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2121-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2121-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2121-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2121-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b2121-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2121-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2121-134"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2121-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2121-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2121-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2121-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2121-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2121-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2121-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2121-138">GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="b2121-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




