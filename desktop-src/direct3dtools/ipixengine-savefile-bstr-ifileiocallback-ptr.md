---
description: Guarda el registro de gráficos en la ubicación especificada.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine:: SaveFile (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538194"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="c660d-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine:: SaveFile (método)</span><span class="sxs-lookup"><span data-stu-id="c660d-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="c660d-104">Guarda el registro de gráficos en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="c660d-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="c660d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c660d-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="c660d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c660d-106">Parameters</span></span>

<span data-ttu-id="c660d-107">*Extensión* </span><span class="sxs-lookup"><span data-stu-id="c660d-107">*FileName* </span></span>  
<span data-ttu-id="c660d-108">Cadena COM que contiene el directorio del registro de gráficos guardado.</span><span class="sxs-lookup"><span data-stu-id="c660d-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="c660d-109">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="c660d-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="c660d-110">La dirección de una funcción que se usa para notificar al host de errores de e/s de archivo durante el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c660d-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="c660d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c660d-111">Return value</span></span>

<span data-ttu-id="c660d-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c660d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c660d-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c660d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c660d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c660d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c660d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c660d-115">Header</span></span></p></td><td><span data-ttu-id="c660d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c660d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c660d-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c660d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c660d-118">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="c660d-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
