---
description: La interfaz IWiaErrorHandler proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para los bits de vista previa o final.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interfaz IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154857"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="5d946-103">Interfaz IWiaErrorHandler</span><span class="sxs-lookup"><span data-stu-id="5d946-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="5d946-104">La interfaz **IWiaErrorHandler** proporciona métodos para controlar los errores que pueden producirse cuando una aplicación solicita datos de imagen, ya sea para los bits de vista previa o final.</span><span class="sxs-lookup"><span data-stu-id="5d946-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="5d946-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d946-105">Members</span></span>

<span data-ttu-id="5d946-106">La interfaz **IWiaErrorHandler** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5d946-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d946-107">**IWiaErrorHandler** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d946-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="5d946-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d946-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d946-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d946-109">Methods</span></span>

<span data-ttu-id="5d946-110">La interfaz **IWiaErrorHandler** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5d946-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="5d946-111">Método</span><span class="sxs-lookup"><span data-stu-id="5d946-111">Method</span></span>                                                                     | <span data-ttu-id="5d946-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d946-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d946-113">**GetStatusDescription**</span><span class="sxs-lookup"><span data-stu-id="5d946-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="5d946-114">Devuelve una cadena que describe el código de estado.</span><span class="sxs-lookup"><span data-stu-id="5d946-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="5d946-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="5d946-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="5d946-116">Controla el estado y los mensajes de error durante las transferencias de datos de imagen y los muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="5d946-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d946-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d946-117">Remarks</span></span>

<span data-ttu-id="5d946-118">El objeto de devolución de llamada de la aplicación puede implementar **IWiaErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="5d946-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="5d946-119">Esta interfaz no está diseñada para controlar los errores detectados fuera de las transferencias de datos de la imagen, por ejemplo, errores al obtener o establecer las propiedades del dispositivo o las devoluciones de llamada no devueltas en un controlador.</span><span class="sxs-lookup"><span data-stu-id="5d946-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d946-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d946-120">Requirements</span></span>



| <span data-ttu-id="5d946-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d946-121">Requirement</span></span> | <span data-ttu-id="5d946-122">Value</span><span class="sxs-lookup"><span data-stu-id="5d946-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d946-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d946-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5d946-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5d946-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d946-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d946-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5d946-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d946-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d946-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d946-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d946-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d946-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="5d946-129">IDL</span><span class="sxs-lookup"><span data-stu-id="5d946-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d946-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d946-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="5d946-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d946-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d946-132"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d946-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
