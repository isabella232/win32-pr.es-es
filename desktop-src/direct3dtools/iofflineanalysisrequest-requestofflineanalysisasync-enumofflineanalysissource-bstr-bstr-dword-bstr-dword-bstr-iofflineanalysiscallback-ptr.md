---
description: Solicita ejecutar el análisis sin conexión con el origen, el manifiesto, los parámetros y el marco especificados.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisRequest::RequestOfflineAnalysisAsync (método)
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
ms.openlocfilehash: 2a8a36f65f2158d03650257cf13458d36330e7fd3184210d99c05200e1731231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981145"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest::RequestOfflineAnalysisAsync (método)

Solicita ejecutar el análisis sin conexión con el origen, el manifiesto, los parámetros y el marco especificados.

## <a name="syntax"></a>Sintaxis


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

## <a name="parameters"></a>Parámetros

*analysisSource*   
Especifica dónde procede el origen del análisis de los informes almacenados en caché o de la reproducción.

*manifestXml*   
Cadena COM que contiene el nombre de ruta de acceso del archivo de manifiesto XML.

*parametersXml*   
Cadena COM que contiene el nombre de ruta de acceso del archivo de parámetros XML.

*Galleta*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*captureFullFileName*   
Cadena COM que contiene la ruta de acceso absoluta del archivo de captura (.vsglog).

*frameNumber*   
Marco especificado.

*outputFullFileName*   
Cadena COM que contiene el nombre de ruta de acceso absoluto del archivo donde se escribe la salida.

*requestCallback*   
Dirección de una devolución de llamada utilizada para notificar al host de resultados.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
