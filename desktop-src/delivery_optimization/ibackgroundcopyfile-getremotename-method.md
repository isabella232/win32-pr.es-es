---
title: Método IBackgroundCopyFile GetRemoteName (Deliveryoptimization. h)
description: Recupera el nombre remoto del archivo.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Método GetRemoteName
- Método GetRemoteName, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079285"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="54e99-106">IBackgroundCopyFile:: GetRemoteName (método)</span><span class="sxs-lookup"><span data-stu-id="54e99-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="54e99-107">Recupera el nombre remoto del archivo.</span><span class="sxs-lookup"><span data-stu-id="54e99-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e99-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54e99-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="54e99-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54e99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e99-110">*ppName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="54e99-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54e99-111">Cadena terminada en null que contiene el nombre remoto del archivo que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="54e99-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="54e99-112">El nombre es completo.</span><span class="sxs-lookup"><span data-stu-id="54e99-112">The name is fully qualified.</span></span> <span data-ttu-id="54e99-113">Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="54e99-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e99-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54e99-114">Return value</span></span>

<span data-ttu-id="54e99-115">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="54e99-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e99-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54e99-116">Remarks</span></span>

<span data-ttu-id="54e99-117">Para cambiar el nombre del archivo remoto, llame al método [**IBackgroundCopyFile2:: SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) .</span><span class="sxs-lookup"><span data-stu-id="54e99-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e99-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e99-118">Requirements</span></span>



| <span data-ttu-id="54e99-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e99-119">Requirement</span></span> | <span data-ttu-id="54e99-120">Value</span><span class="sxs-lookup"><span data-stu-id="54e99-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e99-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54e99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54e99-122">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="54e99-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54e99-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54e99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54e99-124">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="54e99-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="54e99-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54e99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e99-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e99-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="54e99-127">IDL</span><span class="sxs-lookup"><span data-stu-id="54e99-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54e99-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54e99-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="54e99-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="54e99-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="54e99-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54e99-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="54e99-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54e99-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54e99-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54e99-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="54e99-133">IID</span><span class="sxs-lookup"><span data-stu-id="54e99-133">IID</span></span><br/>                      | <span data-ttu-id="54e99-134">IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="54e99-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="54e99-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="54e99-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e99-136">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="54e99-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="54e99-137">**IBackgroundCopyFile::GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="54e99-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

