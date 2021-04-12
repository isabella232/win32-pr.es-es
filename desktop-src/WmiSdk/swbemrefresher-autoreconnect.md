---
description: La propiedad reconexión automática del objeto SWbemRefresher es un valor booleano que indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si se interrumpe la conexión.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Propiedad SWbemRefresher. reconexión automática (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361863"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="a749d-103">Propiedad SWbemRefresher. reconexión automática</span><span class="sxs-lookup"><span data-stu-id="a749d-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="a749d-104">La propiedad **reconexión automática** del objeto [**SWbemRefresher**](swbemrefresher.md) es un valor booleano que indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si se interrumpe la conexión.</span><span class="sxs-lookup"><span data-stu-id="a749d-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="a749d-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a749d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a749d-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a749d-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a749d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a749d-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a749d-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a749d-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a749d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a749d-109">Remarks</span></span>

<span data-ttu-id="a749d-110">La modificación de esta propiedad solo afecta a los objetos del actualizador que están respaldados por un proveedor de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a749d-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="a749d-111">Si el proveedor no es un proveedor de alto rendimiento, el establecimiento de la propiedad **reconexión automática** en **true** no tiene ningún efecto porque el objeto [**SWbemRefresher**](swbemrefresher.md) nunca se vuelve a conectar.</span><span class="sxs-lookup"><span data-stu-id="a749d-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="a749d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a749d-112">Requirements</span></span>



| <span data-ttu-id="a749d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a749d-113">Requirement</span></span> | <span data-ttu-id="a749d-114">Value</span><span class="sxs-lookup"><span data-stu-id="a749d-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a749d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a749d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a749d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a749d-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a749d-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a749d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a749d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a749d-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a749d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a749d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a749d-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a749d-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a749d-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a749d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a749d-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a749d-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a749d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a749d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a749d-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a749d-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a749d-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="a749d-125">CLSID</span></span><br/>                    | <span data-ttu-id="a749d-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="a749d-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="a749d-127">IID</span><span class="sxs-lookup"><span data-stu-id="a749d-127">IID</span></span><br/>                      | <span data-ttu-id="a749d-128">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="a749d-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a749d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a749d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a749d-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="a749d-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




