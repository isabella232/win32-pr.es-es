---
description: Contiene un puntero a la interfaz IMFNetCredentialManager.
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: Propiedad MFNETSOURCE_CREDENTIAL_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154961"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="a95f7-103">\_Propiedad del administrador de credenciales de MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="a95f7-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="a95f7-104">Contiene un puntero a la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="a95f7-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="a95f7-105">Utilice esta propiedad para pasar la implementación de [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) de la aplicación al origen de red.</span><span class="sxs-lookup"><span data-stu-id="a95f7-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="a95f7-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a95f7-106">Data type</span></span>

<span data-ttu-id="a95f7-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a95f7-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a95f7-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a95f7-108">PROPVARIANT member</span></span>

<span data-ttu-id="a95f7-109">**IUnknown** (puntero)</span><span class="sxs-lookup"><span data-stu-id="a95f7-109">**IUnknown** pointer</span></span>

<span data-ttu-id="a95f7-110">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="a95f7-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="a95f7-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="a95f7-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a95f7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a95f7-112">Remarks</span></span>

<span data-ttu-id="a95f7-113">La constante **MFNETSOURCE \_ Credential \_ Manager** define el **GUID** de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a95f7-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="a95f7-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="a95f7-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a95f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a95f7-115">Requirements</span></span>



| <span data-ttu-id="a95f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a95f7-116">Requirement</span></span> | <span data-ttu-id="a95f7-117">Value</span><span class="sxs-lookup"><span data-stu-id="a95f7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a95f7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a95f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a95f7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a95f7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a95f7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a95f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a95f7-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a95f7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a95f7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a95f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a95f7-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a95f7-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a95f7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a95f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95f7-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a95f7-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a95f7-126">Autenticación de origen de red</span><span class="sxs-lookup"><span data-stu-id="a95f7-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="a95f7-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a95f7-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




