---
description: Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: OnNewDataAvailable (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537299"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="bc5d6-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2:: OnNewDataAvailable (método)</span><span class="sxs-lookup"><span data-stu-id="bc5d6-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="bc5d6-104">Solicitudes para indicar que el registro de gráficos tiene nuevos datos dentro de él.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc5d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc5d6-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="bc5d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc5d6-106">Parameters</span></span>

<span data-ttu-id="bc5d6-107">*fSessionEnd* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-107">*fSessionEnd* </span></span>  
<span data-ttu-id="bc5d6-108">True si la sesión ha finalizado; de lo contrario, false.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="bc5d6-109">*fUnloadCurFrame* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="bc5d6-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-110">Not used.</span></span>

<span data-ttu-id="bc5d6-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="bc5d6-112">La posición del archivo, en bytes, a la que se inician los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="bc5d6-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="bc5d6-114">Posición del archivo, en bytes, a la que finalizan los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="bc5d6-115">*iObjectTableDataSize* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="bc5d6-116">El número de bytes contenidos en count4 \_ pObjectTableData.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="bc5d6-117">*count4 \_ pObjectTableData* </span><span class="sxs-lookup"><span data-stu-id="bc5d6-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="bc5d6-118">Búfer que contiene los datos de la tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc5d6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc5d6-119">Return value</span></span>

<span data-ttu-id="bc5d6-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="bc5d6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc5d6-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc5d6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc5d6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc5d6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bc5d6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc5d6-123">Header</span></span></p></td><td><span data-ttu-id="bc5d6-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bc5d6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="bc5d6-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="bc5d6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="bc5d6-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="bc5d6-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
