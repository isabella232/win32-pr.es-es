---
title: Método IBackgroundCopyFile GetLocalName (Deliveryoptimization. h)
description: Recupera el nombre local del archivo.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Método GetLocalName
- Método GetLocalName, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetLocalName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079287"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="6371b-106">IBackgroundCopyFile:: GetLocalName (método)</span><span class="sxs-lookup"><span data-stu-id="6371b-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="6371b-107">Recupera el nombre local del archivo.</span><span class="sxs-lookup"><span data-stu-id="6371b-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6371b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6371b-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="6371b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6371b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6371b-110">*ppName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6371b-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6371b-111">Cadena terminada en null que contiene el nombre del archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="6371b-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="6371b-112">El nombre es completo.</span><span class="sxs-lookup"><span data-stu-id="6371b-112">The name is fully qualified.</span></span> <span data-ttu-id="6371b-113">Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="6371b-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6371b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6371b-114">Return value</span></span>

<span data-ttu-id="6371b-115">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="6371b-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6371b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6371b-116">Requirements</span></span>



| <span data-ttu-id="6371b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6371b-117">Requirement</span></span> | <span data-ttu-id="6371b-118">Value</span><span class="sxs-lookup"><span data-stu-id="6371b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6371b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6371b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6371b-120">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="6371b-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6371b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6371b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6371b-122">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6371b-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6371b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6371b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6371b-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6371b-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6371b-125">IDL</span><span class="sxs-lookup"><span data-stu-id="6371b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6371b-126"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6371b-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6371b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6371b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6371b-128"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6371b-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6371b-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6371b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6371b-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6371b-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6371b-131">IID</span><span class="sxs-lookup"><span data-stu-id="6371b-131">IID</span></span><br/>                      | <span data-ttu-id="6371b-132">IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="6371b-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="6371b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6371b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6371b-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="6371b-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="6371b-135">**IBackgroundCopyFile::GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="6371b-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

