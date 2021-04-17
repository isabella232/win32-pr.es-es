---
description: La interfaz ITAttributeList proporciona métodos para obtener y establecer los atributos no interpretados.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaz ITAttributeList (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690925"
---
# <a name="itattributelist-interface"></a><span data-ttu-id="fa439-103">Interfaz ITAttributeList</span><span class="sxs-lookup"><span data-stu-id="fa439-103">ITAttributeList interface</span></span>

<span data-ttu-id="fa439-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fa439-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa439-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="fa439-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fa439-106">La interfaz **ITAttributeList** proporciona métodos para obtener y establecer los atributos no interpretados.</span><span class="sxs-lookup"><span data-stu-id="fa439-106">The **ITAttributeList** interface supplies methods for getting and setting of uninterpreted attributes.</span></span> <span data-ttu-id="fa439-107">En cuanto a la posición de las cadenas de atributo en un paquete de protocolo de descriptor de sesión (SDP, vea RFC 2327), los métodos suponen que todas las cadenas de atributo existen justo antes de que se especifiquen los atributos multimedia y después de todos los atributos comunes.</span><span class="sxs-lookup"><span data-stu-id="fa439-107">Regarding the position of the attribute strings in a Session Descriptor Protocol (SDP, see RFC 2327) packet, the methods assume that all attribute strings exist just before the media attributes are specified and after all the common attributes.</span></span> <span data-ttu-id="fa439-108">La interfaz **ITAttributeList** se crea llamando a **QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span><span class="sxs-lookup"><span data-stu-id="fa439-108">The **ITAttributeList** interface is created by calling **QueryInterface** on [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).</span></span>

## <a name="members"></a><span data-ttu-id="fa439-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa439-109">Members</span></span>

<span data-ttu-id="fa439-110">La interfaz **ITAttributeList** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fa439-110">The **ITAttributeList** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fa439-111">**ITAttributeList** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fa439-111">**ITAttributeList** also has these types of members:</span></span>

-   [<span data-ttu-id="fa439-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa439-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fa439-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa439-113">Methods</span></span>

<span data-ttu-id="fa439-114">La interfaz **ITAttributeList** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fa439-114">The **ITAttributeList** interface has these methods.</span></span>



| <span data-ttu-id="fa439-115">Método</span><span class="sxs-lookup"><span data-stu-id="fa439-115">Method</span></span>                                                          | <span data-ttu-id="fa439-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa439-116">Description</span></span>                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="fa439-117">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="fa439-117">**Add**</span></span>](itattributelist-add.md)                              | <span data-ttu-id="fa439-118">Agrega el atributo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fa439-118">Adds the attribute at the specified index.</span></span><br/>   |
| [<span data-ttu-id="fa439-119">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="fa439-119">**Delete**</span></span>](itattributelist-delete.md)                        | <span data-ttu-id="fa439-120">Elimina el atributo en el índice especificado</span><span class="sxs-lookup"><span data-stu-id="fa439-120">Deletes the attribute at the specified index</span></span><br/> |
| [<span data-ttu-id="fa439-121">**obtener \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="fa439-121">**get\_AttributeList**</span></span>](itattributelist-get-attributelist.md) | <span data-ttu-id="fa439-122">Obtiene la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="fa439-122">Gets the list of attributes.</span></span><br/>                 |
| [<span data-ttu-id="fa439-123">**obtener \_ recuento**</span><span class="sxs-lookup"><span data-stu-id="fa439-123">**get\_Count**</span></span>](itattributelist-get-count.md)                 | <span data-ttu-id="fa439-124">Obtiene el número de atributos.</span><span class="sxs-lookup"><span data-stu-id="fa439-124">Gets the number of attributes.</span></span><br/>               |
| [<span data-ttu-id="fa439-125">**obtener \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="fa439-125">**get\_Item**</span></span>](itattributelist-get-item.md)                   | <span data-ttu-id="fa439-126">Obtiene el atributo especificado por el índice.</span><span class="sxs-lookup"><span data-stu-id="fa439-126">Gets the attribute specified by the index.</span></span><br/>   |
| [<span data-ttu-id="fa439-127">**Put \_ AttributeList**</span><span class="sxs-lookup"><span data-stu-id="fa439-127">**put\_AttributeList**</span></span>](itattributelist-put-attributelist.md) | <span data-ttu-id="fa439-128">Establece la lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="fa439-128">Sets the list of attributes.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="fa439-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa439-129">Requirements</span></span>



| <span data-ttu-id="fa439-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa439-130">Requirement</span></span> | <span data-ttu-id="fa439-131">Value</span><span class="sxs-lookup"><span data-stu-id="fa439-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa439-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="fa439-132">TAPI version</span></span><br/> | <span data-ttu-id="fa439-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fa439-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fa439-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa439-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fa439-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa439-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa439-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa439-136">Library</span></span><br/>      | <dl> <span data-ttu-id="fa439-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa439-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fa439-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa439-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="fa439-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa439-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

