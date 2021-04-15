---
description: 'Versión remota del método IMFContentProtectionManager:: BeginEnableContent.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: RemoteBeginEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648245"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="1ac36-103">RemoteBeginEnableContent</span><span class="sxs-lookup"><span data-stu-id="1ac36-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="1ac36-104">Versión remota del método [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="1ac36-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="1ac36-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ac36-105">Remarks</span></span>

<span data-ttu-id="1ac36-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="1ac36-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1ac36-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="1ac36-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1ac36-108">Si se llama a [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1ac36-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac36-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ac36-109">Requirements</span></span>



| <span data-ttu-id="1ac36-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ac36-110">Requirement</span></span> | <span data-ttu-id="1ac36-111">Value</span><span class="sxs-lookup"><span data-stu-id="1ac36-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac36-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ac36-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1ac36-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ac36-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ac36-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ac36-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1ac36-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ac36-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ac36-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ac36-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ac36-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ac36-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="1ac36-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ac36-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ac36-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ac36-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1ac36-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ac36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac36-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="1ac36-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




