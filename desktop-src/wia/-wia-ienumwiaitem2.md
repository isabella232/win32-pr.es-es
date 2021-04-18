---
description: Lo usan las aplicaciones para enumerar los objetos IWiaItem2 en la carpeta actual del árbol de elementos.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interfaz IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652477"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="4a1ec-103">Interfaz IEnumWiaItem2</span><span class="sxs-lookup"><span data-stu-id="4a1ec-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="4a1ec-104">Lo usan las aplicaciones para enumerar los objetos [**IWiaItem2**](-wia-iwiaitem2.md) en la carpeta actual del árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="4a1ec-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="4a1ec-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a1ec-105">Members</span></span>

<span data-ttu-id="4a1ec-106">La interfaz **IEnumWiaItem2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a1ec-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a1ec-107">**IEnumWiaItem2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a1ec-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="4a1ec-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a1ec-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a1ec-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a1ec-109">Methods</span></span>

<span data-ttu-id="4a1ec-110">La interfaz **IEnumWiaItem2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a1ec-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="4a1ec-111">Método</span><span class="sxs-lookup"><span data-stu-id="4a1ec-111">Method</span></span>                                          | <span data-ttu-id="4a1ec-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a1ec-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a1ec-113">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="4a1ec-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="4a1ec-114">Crea una instancia adicional de la interfaz **IEnumWiaItem2** y le devuelve un puntero.</span><span class="sxs-lookup"><span data-stu-id="4a1ec-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="4a1ec-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4a1ec-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="4a1ec-116">Devuelve el número de elementos almacenados por este enumerador.</span><span class="sxs-lookup"><span data-stu-id="4a1ec-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="4a1ec-117">**Next**</span><span class="sxs-lookup"><span data-stu-id="4a1ec-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="4a1ec-118">Rellena una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1ec-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="4a1ec-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4a1ec-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="4a1ec-120">Restablece la referencia de enumeración al primer objeto [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="4a1ec-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="4a1ec-121">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="4a1ec-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="4a1ec-122">Omite el número especificado de elementos durante una enumeración de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a1ec-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4a1ec-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a1ec-123">Requirements</span></span>



| <span data-ttu-id="4a1ec-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a1ec-124">Requirement</span></span> | <span data-ttu-id="4a1ec-125">Value</span><span class="sxs-lookup"><span data-stu-id="4a1ec-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1ec-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a1ec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1ec-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a1ec-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a1ec-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a1ec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1ec-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a1ec-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a1ec-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a1ec-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a1ec-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a1ec-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a1ec-132">IDL</span><span class="sxs-lookup"><span data-stu-id="4a1ec-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a1ec-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a1ec-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
