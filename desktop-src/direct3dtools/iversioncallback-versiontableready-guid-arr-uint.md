---
description: Función de devolución de llamada que se usa para notificar al host qué interfaces se admiten.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IVersionCallback:: VersionTableReady (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4f31f8b4619d74f6f491f6be8faf7ddd457ee82c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152393"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span data-ttu-id="119a3-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback:: VersionTableReady (método)</span><span class="sxs-lookup"><span data-stu-id="119a3-103"><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>IVersionCallback::VersionTableReady method</span></span>

<span data-ttu-id="119a3-104">Función de devolución de llamada que se usa para notificar al host qué interfaces se admiten.</span><span class="sxs-lookup"><span data-stu-id="119a3-104">A callback function used to notify the host of which interfaces are supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="119a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="119a3-105">Syntax</span></span>


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a><span data-ttu-id="119a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="119a3-106">Parameters</span></span>

<span data-ttu-id="119a3-107">*count1 \_ interfaceIds* </span><span class="sxs-lookup"><span data-stu-id="119a3-107">*count1\_interfaceIds* </span></span>  
<span data-ttu-id="119a3-108">Una matriz que contiene los GUID de los identificadores de interfaz admitidos.</span><span class="sxs-lookup"><span data-stu-id="119a3-108">An array containing the GUIDs of supported interface IDs.</span></span>

<span data-ttu-id="119a3-109">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="119a3-109">*count* </span></span>  
<span data-ttu-id="119a3-110">Número de GUID pasados en count1 \_ interfaceIds.</span><span class="sxs-lookup"><span data-stu-id="119a3-110">The number of GUIDs passed in count1\_interfaceIds.</span></span>

## <a name="return-value"></a><span data-ttu-id="119a3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="119a3-111">Return value</span></span>

<span data-ttu-id="119a3-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="119a3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="119a3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="119a3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="119a3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="119a3-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="119a3-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="119a3-115">Header</span></span></p></td><td><span data-ttu-id="119a3-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="119a3-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="119a3-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="119a3-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="119a3-118">**IVersionCallback**</span><span class="sxs-lookup"><span data-stu-id="119a3-118">**IVersionCallback**</span></span>](/windows/desktop/direct3dtools/iversioncallback)

 

 
