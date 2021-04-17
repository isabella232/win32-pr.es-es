---
description: 'Versión remota del método IMFPMPHost:: CreateObjectByCLSID.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: RemoteCreateObjectByCLSID (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666709"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="5f5bd-103">RemoteCreateObjectByCLSID</span><span class="sxs-lookup"><span data-stu-id="5f5bd-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="5f5bd-104">Versión remota del método [**IMFPMPHost:: CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="5f5bd-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="5f5bd-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f5bd-105">Remarks</span></span>

<span data-ttu-id="5f5bd-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="5f5bd-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="5f5bd-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5f5bd-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="5f5bd-108">Si se llama a [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="5f5bd-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5bd-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f5bd-109">Requirements</span></span>



| <span data-ttu-id="5f5bd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5bd-110">Requirement</span></span> | <span data-ttu-id="5f5bd-111">Value</span><span class="sxs-lookup"><span data-stu-id="5f5bd-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5bd-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f5bd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5bd-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f5bd-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f5bd-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f5bd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5bd-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f5bd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f5bd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f5bd-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5bd-117"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f5bd-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="5f5bd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f5bd-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f5bd-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f5bd-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5f5bd-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f5bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5bd-121">**IMFPMPHost**</span><span class="sxs-lookup"><span data-stu-id="5f5bd-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="5f5bd-122">Sesión de medios de PMP</span><span class="sxs-lookup"><span data-stu-id="5f5bd-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="5f5bd-123">Ruta de acceso a medios protegidos</span><span class="sxs-lookup"><span data-stu-id="5f5bd-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




