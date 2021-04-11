---
description: La interfaz IWiaTransfer proporciona transferencia de datos basada en secuencias.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interfaz IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275457"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="060e9-103">Interfaz IWiaTransfer</span><span class="sxs-lookup"><span data-stu-id="060e9-103">IWiaTransfer interface</span></span>

<span data-ttu-id="060e9-104">La interfaz **IWiaTransfer** proporciona transferencia de datos basada en secuencias.</span><span class="sxs-lookup"><span data-stu-id="060e9-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="060e9-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="060e9-105">Members</span></span>

<span data-ttu-id="060e9-106">La interfaz **IWiaTransfer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="060e9-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="060e9-107">**IWiaTransfer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="060e9-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="060e9-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="060e9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="060e9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="060e9-109">Methods</span></span>

<span data-ttu-id="060e9-110">La interfaz **IWiaTransfer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="060e9-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="060e9-111">Método</span><span class="sxs-lookup"><span data-stu-id="060e9-111">Method</span></span>                                                                 | <span data-ttu-id="060e9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="060e9-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="060e9-113">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="060e9-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="060e9-114">Cancela la operación de transferencia actual.</span><span class="sxs-lookup"><span data-stu-id="060e9-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="060e9-115">**Descargar**</span><span class="sxs-lookup"><span data-stu-id="060e9-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="060e9-116">Inicia una descarga de datos en el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="060e9-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="060e9-117">**\_Información de formato de EnumWIA \_**</span><span class="sxs-lookup"><span data-stu-id="060e9-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="060e9-118">Crea un enumerador para los formatos de transferencia que admite el dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="060e9-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="060e9-119">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="060e9-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="060e9-120">Inicia una carga de datos de un único elemento del llamador.</span><span class="sxs-lookup"><span data-stu-id="060e9-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="060e9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="060e9-121">Remarks</span></span>

<span data-ttu-id="060e9-122">La interfaz **IWiaTransfer** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="060e9-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="060e9-123">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="060e9-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="060e9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="060e9-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="060e9-125">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="060e9-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="060e9-126">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="060e9-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="060e9-127">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="060e9-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="060e9-128">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="060e9-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="060e9-129">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="060e9-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="060e9-130">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="060e9-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="060e9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="060e9-131">Requirements</span></span>



| <span data-ttu-id="060e9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="060e9-132">Requirement</span></span> | <span data-ttu-id="060e9-133">Value</span><span class="sxs-lookup"><span data-stu-id="060e9-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="060e9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060e9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="060e9-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="060e9-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="060e9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060e9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="060e9-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="060e9-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="060e9-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="060e9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="060e9-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="060e9-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="060e9-140">IDL</span><span class="sxs-lookup"><span data-stu-id="060e9-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="060e9-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="060e9-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="060e9-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="060e9-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="060e9-143"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="060e9-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
