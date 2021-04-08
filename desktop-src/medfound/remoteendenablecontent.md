---
description: 'Versión remota del método IMFContentProtectionManager:: EndEnableContent.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: RemoteEndEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908373"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="cb950-103">RemoteEndEnableContent</span><span class="sxs-lookup"><span data-stu-id="cb950-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="cb950-104">Versión remota del método [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="cb950-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="cb950-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb950-105">Remarks</span></span>

<span data-ttu-id="cb950-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="cb950-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="cb950-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cb950-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="cb950-108">Si se llama a [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="cb950-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb950-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb950-109">Requirements</span></span>



| <span data-ttu-id="cb950-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb950-110">Requirement</span></span> | <span data-ttu-id="cb950-111">Value</span><span class="sxs-lookup"><span data-stu-id="cb950-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb950-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb950-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cb950-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb950-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb950-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb950-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cb950-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb950-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb950-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb950-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb950-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb950-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb950-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb950-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb950-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb950-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="cb950-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb950-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb950-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="cb950-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




