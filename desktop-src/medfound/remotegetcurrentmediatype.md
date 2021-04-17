---
description: 'Versión remota del método IMFMediaTypeHandler:: GetCurrentMediaType.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: RemoteGetCurrentMediaType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707527"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="3ef4e-103">RemoteGetCurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="3ef4e-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="3ef4e-104">Versión remota del método [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) .</span><span class="sxs-lookup"><span data-stu-id="3ef4e-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="3ef4e-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ef4e-105">Remarks</span></span>

<span data-ttu-id="3ef4e-106">Las aplicaciones no pueden llamar directamente a este método y los objetos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3ef4e-107">El método no aparece en la tabla vtable de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3ef4e-108">Si se llama a [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) a través de los límites del proceso, el archivo DLL de Media Foundation proxy/stub traduce la llamada en una llamada al método remoto y, a continuación, la convierte de nuevo.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="3ef4e-109">Esta interfaz está disponible en las siguientes plataformas si están instalados los componentes redistribuibles del SDK de Windows Media Format 11:</span><span class="sxs-lookup"><span data-stu-id="3ef4e-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="3ef4e-110">Windows XP con Service Pack 2 (SP2) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="3ef4e-111">Windows XP Media Center Edition 2005 con KB900325 (Windows XP Media Center Edition 2005) y KB925766 (paquete acumulativo de actualizaciones de octubre de 2006 para Windows XP Media Center Edition) instalado.</span><span class="sxs-lookup"><span data-stu-id="3ef4e-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef4e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ef4e-112">Requirements</span></span>



| <span data-ttu-id="3ef4e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef4e-113">Requirement</span></span> | <span data-ttu-id="3ef4e-114">Value</span><span class="sxs-lookup"><span data-stu-id="3ef4e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef4e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef4e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3ef4e-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="3ef4e-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3ef4e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ef4e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3ef4e-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ef4e-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3ef4e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ef4e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ef4e-120"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ef4e-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3ef4e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ef4e-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ef4e-122"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ef4e-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3ef4e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ef4e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef4e-124">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="3ef4e-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




