---
description: Actualiza el estado inicial de un objeto. por ejemplo, una textura o un sombreador.
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine4:: UpdateObject (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494692"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="495e4-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4:: UpdateObject (método)</span><span class="sxs-lookup"><span data-stu-id="495e4-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="495e4-104">Actualiza el estado inicial de un objeto. por ejemplo, una textura o un sombreador.</span><span class="sxs-lookup"><span data-stu-id="495e4-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="495e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="495e4-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="495e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="495e4-106">Parameters</span></span>

<span data-ttu-id="495e4-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="495e4-107">*objectAddress* </span></span>  
<span data-ttu-id="495e4-108">IDENTIFICADOR del objeto que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="495e4-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="495e4-109">*ajusta* </span><span class="sxs-lookup"><span data-stu-id="495e4-109">*size* </span></span>  
<span data-ttu-id="495e4-110">Tamaño de la carga de actualización en bytes.</span><span class="sxs-lookup"><span data-stu-id="495e4-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="495e4-111">*\_búfer count1* </span><span class="sxs-lookup"><span data-stu-id="495e4-111">*count1\_buffer* </span></span>  
<span data-ttu-id="495e4-112">Carga de actualización.</span><span class="sxs-lookup"><span data-stu-id="495e4-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="495e4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="495e4-113">Return value</span></span>

<span data-ttu-id="495e4-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="495e4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="495e4-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="495e4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="495e4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="495e4-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="495e4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="495e4-117">Header</span></span></p></td><td><span data-ttu-id="495e4-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="495e4-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="495e4-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="495e4-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="495e4-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="495e4-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 
