---
description: El método GetCurrentDir devuelve una ruta de acceso absoluta al directorio seleccionado actualmente.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'ISCardFileAccess:: GetCurrentDir (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279313"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="9a653-103">ISCardFileAccess:: GetCurrentDir (método)</span><span class="sxs-lookup"><span data-stu-id="9a653-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="9a653-104">\[El método **GetCurrentDir** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9a653-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9a653-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a653-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a653-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="9a653-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9a653-107">El método **GetCurrentDir** devuelve una ruta de acceso absoluta al directorio seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="9a653-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a653-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a653-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="9a653-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a653-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a653-110">*pbstrPathSpec* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9a653-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a653-111">Puntero a un BSTR que contendrá la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="9a653-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a653-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a653-112">Return value</span></span>

<span data-ttu-id="9a653-113">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="9a653-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9a653-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9a653-114">Return code</span></span>                                                                                   | <span data-ttu-id="9a653-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a653-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9a653-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9a653-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a653-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="9a653-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9a653-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9a653-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9a653-119">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="9a653-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9a653-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a653-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9a653-121">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="9a653-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9a653-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a653-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a653-123">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="9a653-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9a653-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a653-124">Remarks</span></span>

<span data-ttu-id="9a653-125">Para cambiar el directorio actual, llame a [**ChangeDir**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="9a653-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="9a653-126">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="9a653-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="9a653-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a653-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9a653-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a653-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a653-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a653-129">Requirements</span></span>



| <span data-ttu-id="9a653-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a653-130">Requirement</span></span> | <span data-ttu-id="9a653-131">Value</span><span class="sxs-lookup"><span data-stu-id="9a653-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a653-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a653-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a653-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9a653-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9a653-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a653-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a653-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a653-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9a653-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9a653-136">End of client support</span></span><br/>    | <span data-ttu-id="9a653-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a653-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9a653-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9a653-138">End of server support</span></span><br/>    | <span data-ttu-id="9a653-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a653-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9a653-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a653-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a653-141">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="9a653-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="9a653-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="9a653-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
