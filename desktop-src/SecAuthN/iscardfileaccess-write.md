---
description: El método Write escribe datos en un archivo abierto actual.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'ISCardFileAccess:: Write (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156300"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="3e07f-103">ISCardFileAccess:: Write (método)</span><span class="sxs-lookup"><span data-stu-id="3e07f-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="3e07f-104">\[El método de **escritura** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3e07f-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e07f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3e07f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3e07f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3e07f-107">El método **Write** escribe datos en un archivo abierto actual.</span><span class="sxs-lookup"><span data-stu-id="3e07f-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e07f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e07f-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="3e07f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e07f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e07f-110">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e07f-111">Identificador de un archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="3e07f-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="3e07f-112">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e07f-113">Objeto/datos que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="3e07f-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="3e07f-114">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e07f-115">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="3e07f-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="3e07f-116">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="3e07f-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e07f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e07f-117">Return value</span></span>

<span data-ttu-id="3e07f-118">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="3e07f-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3e07f-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e07f-119">Return code</span></span>                                                                                   | <span data-ttu-id="3e07f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e07f-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e07f-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e07f-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3e07f-122">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e07f-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3e07f-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e07f-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3e07f-124">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="3e07f-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3e07f-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e07f-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3e07f-126">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="3e07f-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3e07f-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3e07f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3e07f-128">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="3e07f-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3e07f-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e07f-129">Remarks</span></span>

<span data-ttu-id="3e07f-130">Para abrir o cerrar un archivo, llame a [**abrir**](iscardfileaccess-open.md) o [**cerrar**](iscardfileaccess-close.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3e07f-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="3e07f-131">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="3e07f-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="3e07f-132">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e07f-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3e07f-133">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3e07f-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e07f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e07f-134">Requirements</span></span>



| <span data-ttu-id="3e07f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e07f-135">Requirement</span></span> | <span data-ttu-id="3e07f-136">Value</span><span class="sxs-lookup"><span data-stu-id="3e07f-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e07f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e07f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e07f-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3e07f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e07f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e07f-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e07f-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3e07f-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3e07f-141">End of client support</span></span><br/>    | <span data-ttu-id="3e07f-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e07f-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3e07f-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3e07f-143">End of server support</span></span><br/>    | <span data-ttu-id="3e07f-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e07f-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3e07f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e07f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e07f-146">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="3e07f-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="3e07f-147">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="3e07f-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="3e07f-148">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="3e07f-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
