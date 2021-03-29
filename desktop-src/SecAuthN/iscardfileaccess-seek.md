---
description: El método Seek selecciona el objeto del que se realizará el acceso (lectura y escritura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'ISCardFileAccess:: Seek (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814198"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="16c0a-103">ISCardFileAccess:: Seek (método)</span><span class="sxs-lookup"><span data-stu-id="16c0a-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="16c0a-104">\[El método **Seek** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="16c0a-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="16c0a-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="16c0a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="16c0a-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="16c0a-107">El método **Seek** selecciona el objeto del que se realizará el acceso (lectura y escritura).</span><span class="sxs-lookup"><span data-stu-id="16c0a-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c0a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16c0a-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="16c0a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16c0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c0a-110">*hFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c0a-111">Identificador del archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="16c0a-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="16c0a-112">*Buscar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c0a-113">Ubicación donde debe comenzar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="16c0a-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="16c0a-114">Value</span><span class="sxs-lookup"><span data-stu-id="16c0a-114">Value</span></span>                                                                                                | <span data-ttu-id="16c0a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="16c0a-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="16c0a-116"><dt>SC \_ Buscar \_ desde el \_ principio</dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="16c0a-117">Comienza la búsqueda al principio.</span><span class="sxs-lookup"><span data-stu-id="16c0a-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="16c0a-118"><dt>SC \_ Buscar \_ desde el \_ final </dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="16c0a-119">Comience la búsqueda desde el final.</span><span class="sxs-lookup"><span data-stu-id="16c0a-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="16c0a-120"><dt>referencia de SC \_ Seek \_ relativa</dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="16c0a-121">Comienza la búsqueda desde la posición actual.</span><span class="sxs-lookup"><span data-stu-id="16c0a-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="16c0a-122">*lOffset* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c0a-123">Número de objetos de datos del objeto de referencia.</span><span class="sxs-lookup"><span data-stu-id="16c0a-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c0a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16c0a-124">Return value</span></span>

<span data-ttu-id="16c0a-125">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="16c0a-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="16c0a-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="16c0a-126">Return code</span></span>                                                                                   | <span data-ttu-id="16c0a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="16c0a-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="16c0a-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="16c0a-129">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="16c0a-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="16c0a-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="16c0a-131">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="16c0a-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="16c0a-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="16c0a-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="16c0a-133">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="16c0a-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="16c0a-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16c0a-134">Remarks</span></span>

<span data-ttu-id="16c0a-135">Para leer o escribir en un archivo, llame a [**Read**](iscardfileaccess-read.md) o [**Write**](iscardfileaccess-write.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="16c0a-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="16c0a-136">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="16c0a-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="16c0a-137">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16c0a-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="16c0a-138">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="16c0a-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16c0a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c0a-139">Requirements</span></span>



| <span data-ttu-id="16c0a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c0a-140">Requirement</span></span> | <span data-ttu-id="16c0a-141">Value</span><span class="sxs-lookup"><span data-stu-id="16c0a-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16c0a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c0a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="16c0a-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="16c0a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16c0a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="16c0a-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="16c0a-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="16c0a-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="16c0a-146">End of client support</span></span><br/>    | <span data-ttu-id="16c0a-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="16c0a-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="16c0a-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="16c0a-148">End of server support</span></span><br/>    | <span data-ttu-id="16c0a-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16c0a-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="16c0a-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="16c0a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c0a-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="16c0a-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="16c0a-152">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="16c0a-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="16c0a-153">**Escritura**</span><span class="sxs-lookup"><span data-stu-id="16c0a-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
