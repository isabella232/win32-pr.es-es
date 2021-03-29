---
description: Proporciona funcionalidad para obtener el IMFDXGIDeviceManager del receptor de representación de vídeo Microsoft Media Foundation.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interfaz IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811042"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="f3bd5-103">Interfaz IMFDXGIDeviceManagerSource</span><span class="sxs-lookup"><span data-stu-id="f3bd5-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="f3bd5-104">Proporciona funcionalidad para obtener el [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) del receptor de representación de vídeo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="f3bd5-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3bd5-105">Members</span></span>

<span data-ttu-id="f3bd5-106">La interfaz **IMFDXGIDeviceManagerSource** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f3bd5-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3bd5-107">**IMFDXGIDeviceManagerSource** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3bd5-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="f3bd5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3bd5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f3bd5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3bd5-109">Methods</span></span>

<span data-ttu-id="f3bd5-110">La interfaz **IMFDXGIDeviceManagerSource** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="f3bd5-111">Método</span><span class="sxs-lookup"><span data-stu-id="f3bd5-111">Method</span></span>                                                      | <span data-ttu-id="f3bd5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3bd5-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3bd5-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="f3bd5-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="f3bd5-114">Obtiene el [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) del receptor de representación de vídeo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f3bd5-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f3bd5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3bd5-115">Requirements</span></span>



| <span data-ttu-id="f3bd5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3bd5-116">Requirement</span></span> | <span data-ttu-id="f3bd5-117">Value</span><span class="sxs-lookup"><span data-stu-id="f3bd5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3bd5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bd5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bd5-119">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="f3bd5-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f3bd5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bd5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bd5-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f3bd5-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="f3bd5-122">IDL</span><span class="sxs-lookup"><span data-stu-id="f3bd5-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3bd5-123"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3bd5-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3bd5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3bd5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3bd5-125">Interfaces de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3bd5-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
