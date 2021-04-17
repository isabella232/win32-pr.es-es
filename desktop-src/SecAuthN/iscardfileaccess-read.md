---
description: El método Read Lee y devuelve los datos especificados de un archivo determinado.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'ISCardFileAccess:: Read (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277019"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="68b52-103">ISCardFileAccess:: Read (método)</span><span class="sxs-lookup"><span data-stu-id="68b52-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="68b52-104">\[El método **Read** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="68b52-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="68b52-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68b52-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68b52-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="68b52-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="68b52-107">El método **Read** Lee y devuelve los datos especificados de un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="68b52-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b52-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68b52-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="68b52-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b52-110">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68b52-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b52-111">Identificador del archivo abierto al que se va a tener acceso.</span><span class="sxs-lookup"><span data-stu-id="68b52-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="68b52-112">*lBytesToRead* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68b52-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b52-113">Longitud de los datos que se van a leer (en) o el número de bytes leídos (out).</span><span class="sxs-lookup"><span data-stu-id="68b52-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="68b52-114">Devuelve una lista de archivos como una matriz de BSTR.</span><span class="sxs-lookup"><span data-stu-id="68b52-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="68b52-115">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="68b52-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68b52-116">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="68b52-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="68b52-117">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="68b52-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="68b52-118">*ppBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68b52-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68b52-119">Un objeto [**IByteBuffer**](ibytebuffer.md) que contiene los datos leídos.</span><span class="sxs-lookup"><span data-stu-id="68b52-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b52-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b52-120">Return value</span></span>

<span data-ttu-id="68b52-121">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="68b52-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="68b52-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68b52-122">Return code</span></span>                                                                                   | <span data-ttu-id="68b52-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="68b52-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="68b52-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="68b52-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68b52-125">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="68b52-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="68b52-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="68b52-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="68b52-127">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="68b52-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="68b52-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="68b52-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="68b52-129">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="68b52-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="68b52-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68b52-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68b52-131">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="68b52-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="68b52-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68b52-132">Remarks</span></span>

<span data-ttu-id="68b52-133">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="68b52-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="68b52-134">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68b52-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="68b52-135">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="68b52-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68b52-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b52-136">Requirements</span></span>



| <span data-ttu-id="68b52-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b52-137">Requirement</span></span> | <span data-ttu-id="68b52-138">Value</span><span class="sxs-lookup"><span data-stu-id="68b52-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68b52-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b52-139">Minimum supported client</span></span><br/> | <span data-ttu-id="68b52-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="68b52-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="68b52-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b52-141">Minimum supported server</span></span><br/> | <span data-ttu-id="68b52-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="68b52-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="68b52-143">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="68b52-143">End of client support</span></span><br/>    | <span data-ttu-id="68b52-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68b52-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="68b52-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="68b52-145">End of server support</span></span><br/>    | <span data-ttu-id="68b52-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68b52-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="68b52-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="68b52-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b52-148">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="68b52-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
