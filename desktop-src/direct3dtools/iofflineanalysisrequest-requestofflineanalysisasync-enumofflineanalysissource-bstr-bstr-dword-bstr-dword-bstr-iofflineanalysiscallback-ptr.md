---
description: Solicita que se ejecute el análisis sin conexión con el origen especificado, el manifiesto, los parámetros y el marco especificado.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d027b9ec463c0bebfefca3ee7f9af4b50c514755
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422952"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span data-ttu-id="8065b-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync (método)</span><span class="sxs-lookup"><span data-stu-id="8065b-103"><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync method</span></span>

<span data-ttu-id="8065b-104">Solicita que se ejecute el análisis sin conexión con el origen especificado, el manifiesto, los parámetros y el marco especificado.</span><span class="sxs-lookup"><span data-stu-id="8065b-104">Requests to run offline analysis with the specified source, manifest, parameters and of the specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="8065b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8065b-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="8065b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8065b-106">Parameters</span></span>

<span data-ttu-id="8065b-107">*analysisSource* </span><span class="sxs-lookup"><span data-stu-id="8065b-107">*analysisSource* </span></span>  
<span data-ttu-id="8065b-108">Especifica donde el origen del análisis procede de los informes almacenados en caché o de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="8065b-108">Specfies where the analysis source come from cached reports or from playback.</span></span>

<span data-ttu-id="8065b-109">*manifestXml* </span><span class="sxs-lookup"><span data-stu-id="8065b-109">*manifestXml* </span></span>  
<span data-ttu-id="8065b-110">Cadena COM que contiene la ruta de acceso del archivo de manifiesto XML.</span><span class="sxs-lookup"><span data-stu-id="8065b-110">A COM string containing the pathname of the XML manifest file.</span></span>

<span data-ttu-id="8065b-111">*parametersXml* </span><span class="sxs-lookup"><span data-stu-id="8065b-111">*parametersXml* </span></span>  
<span data-ttu-id="8065b-112">Cadena COM que contiene la ruta de acceso del archivo de parámetros XML.</span><span class="sxs-lookup"><span data-stu-id="8065b-112">A COM string containing the pathname of the XML parameters file.</span></span>

<span data-ttu-id="8065b-113">*ellas* </span><span class="sxs-lookup"><span data-stu-id="8065b-113">*cookie* </span></span>  
<span data-ttu-id="8065b-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="8065b-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="8065b-115">*captureFullFileName* </span><span class="sxs-lookup"><span data-stu-id="8065b-115">*captureFullFileName* </span></span>  
<span data-ttu-id="8065b-116">Cadena COM que contiene la ruta de acceso absoluta del archivo de captura (. vsglog).</span><span class="sxs-lookup"><span data-stu-id="8065b-116">A COM string containing the absolute pathname of the capture file (.vsglog).</span></span>

<span data-ttu-id="8065b-117">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="8065b-117">*frameNumber* </span></span>  
<span data-ttu-id="8065b-118">Marco especificado.</span><span class="sxs-lookup"><span data-stu-id="8065b-118">The specified frame.</span></span>

<span data-ttu-id="8065b-119">*outputFullFileName* </span><span class="sxs-lookup"><span data-stu-id="8065b-119">*outputFullFileName* </span></span>  
<span data-ttu-id="8065b-120">Cadena COM que contiene la ruta de acceso absoluta del archivo donde se escribe la salida.</span><span class="sxs-lookup"><span data-stu-id="8065b-120">A COM string containing the absolute pathname of the file where output is written.</span></span>

<span data-ttu-id="8065b-121">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="8065b-121">*requestCallback* </span></span>  
<span data-ttu-id="8065b-122">La dirección de una devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="8065b-122">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="8065b-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8065b-123">Return value</span></span>

<span data-ttu-id="8065b-124">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8065b-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8065b-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8065b-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8065b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8065b-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8065b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8065b-127">Header</span></span></p></td><td><span data-ttu-id="8065b-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8065b-128">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8065b-129"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="8065b-129"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8065b-130">**IOfflineAnalysisRequest**</span><span class="sxs-lookup"><span data-stu-id="8065b-130">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
