---
description: Solicitud para actualizar el estado inicial de un objeto; por ejemplo, una textura o un sombreador.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IUpdateObject:: UpdateObject (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495251"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="e55e6-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject:: UpdateObject (método)</span><span class="sxs-lookup"><span data-stu-id="e55e6-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="e55e6-104">Solicitud para actualizar el estado inicial de un objeto; por ejemplo, una textura o un sombreador.</span><span class="sxs-lookup"><span data-stu-id="e55e6-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e55e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e55e6-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="e55e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e55e6-106">Parameters</span></span>

<span data-ttu-id="e55e6-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="e55e6-107">*objectAddress* </span></span>  
<span data-ttu-id="e55e6-108">IDENTIFICADOR del objeto que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="e55e6-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="e55e6-109">*ajusta* </span><span class="sxs-lookup"><span data-stu-id="e55e6-109">*size* </span></span>  
<span data-ttu-id="e55e6-110">Tamaño de la carga de actualización en bytes.</span><span class="sxs-lookup"><span data-stu-id="e55e6-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="e55e6-111">*\_búfer count1* </span><span class="sxs-lookup"><span data-stu-id="e55e6-111">*count1\_buffer* </span></span>  
<span data-ttu-id="e55e6-112">Carga de actualización.</span><span class="sxs-lookup"><span data-stu-id="e55e6-112">The update payload.</span></span>

<span data-ttu-id="e55e6-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="e55e6-113">*pCallback* </span></span>  
<span data-ttu-id="e55e6-114">La dirección de una función que se usa para notificar al host que se actualizó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e55e6-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="e55e6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e55e6-115">Return value</span></span>

<span data-ttu-id="e55e6-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e55e6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e55e6-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e55e6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e55e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e55e6-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e55e6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e55e6-119">Header</span></span></p></td><td><span data-ttu-id="e55e6-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e55e6-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e55e6-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="e55e6-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e55e6-122">**IUpdateObject**</span><span class="sxs-lookup"><span data-stu-id="e55e6-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
