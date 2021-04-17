---
description: Devolución de llamada que notifica al host la información de malla escrita por la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback3:: MeshFileReadyCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677101"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="92a22-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3:: MeshFileReadyCallback (método)</span><span class="sxs-lookup"><span data-stu-id="92a22-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="92a22-104">Devolución de llamada que notifica al host la información de malla escrita por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="92a22-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92a22-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="92a22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92a22-106">Parameters</span></span>

<span data-ttu-id="92a22-107">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="92a22-107">*meshFilename* </span></span>  
<span data-ttu-id="92a22-108">Cadena COM que contiene la ruta de acceso del archivo donde se escriben los datos de la malla.</span><span class="sxs-lookup"><span data-stu-id="92a22-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="92a22-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92a22-109">Return value</span></span>

<span data-ttu-id="92a22-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="92a22-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92a22-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92a22-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a22-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a22-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="92a22-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92a22-113">Header</span></span></p></td><td><span data-ttu-id="92a22-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="92a22-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="92a22-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="92a22-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="92a22-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="92a22-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
