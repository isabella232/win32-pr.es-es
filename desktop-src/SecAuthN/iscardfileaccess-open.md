---
description: El método Open abre el archivo especificado para su uso posterior.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'ISCardFileAccess:: Open (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156301"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="006eb-103">ISCardFileAccess:: Open (método)</span><span class="sxs-lookup"><span data-stu-id="006eb-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="006eb-104">\[El método **Open** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="006eb-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="006eb-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="006eb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="006eb-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="006eb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="006eb-107">El método **Open** abre el archivo especificado para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="006eb-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="006eb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="006eb-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="006eb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="006eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006eb-110">*refType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="006eb-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="006eb-111">Tipo de referencia que se usa en *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="006eb-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="006eb-112">**\_tipo SC \_ por \_ nombre**</span><span class="sxs-lookup"><span data-stu-id="006eb-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="006eb-113">**\_tipo SC \_ por \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="006eb-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="006eb-114">**\_tipo SC \_ por \_ corto**</span><span class="sxs-lookup"><span data-stu-id="006eb-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="006eb-115">**\_tipo SC \_ por \_ cualquier**</span><span class="sxs-lookup"><span data-stu-id="006eb-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="006eb-116">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="006eb-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="006eb-117">Archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="006eb-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="006eb-118">*phFile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="006eb-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="006eb-119">Puntero a un \_ archivo HSCARD que va a contener el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="006eb-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="006eb-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="006eb-120">Return value</span></span>

<span data-ttu-id="006eb-121">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="006eb-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="006eb-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="006eb-122">Return code</span></span>                                                                                   | <span data-ttu-id="006eb-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="006eb-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="006eb-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="006eb-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="006eb-125">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="006eb-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="006eb-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="006eb-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="006eb-127">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="006eb-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="006eb-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="006eb-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="006eb-129">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="006eb-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="006eb-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="006eb-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="006eb-131">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="006eb-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="006eb-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="006eb-132">Remarks</span></span>

<span data-ttu-id="006eb-133">Para cerrar un archivo, llame a [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="006eb-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="006eb-134">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="006eb-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="006eb-135">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="006eb-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="006eb-136">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="006eb-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="006eb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006eb-137">Requirements</span></span>



| <span data-ttu-id="006eb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="006eb-138">Requirement</span></span> | <span data-ttu-id="006eb-139">Value</span><span class="sxs-lookup"><span data-stu-id="006eb-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="006eb-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="006eb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="006eb-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="006eb-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="006eb-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="006eb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="006eb-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="006eb-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="006eb-144">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="006eb-144">End of client support</span></span><br/>    | <span data-ttu-id="006eb-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="006eb-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="006eb-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="006eb-146">End of server support</span></span><br/>    | <span data-ttu-id="006eb-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="006eb-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="006eb-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="006eb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006eb-149">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="006eb-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="006eb-150">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="006eb-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
