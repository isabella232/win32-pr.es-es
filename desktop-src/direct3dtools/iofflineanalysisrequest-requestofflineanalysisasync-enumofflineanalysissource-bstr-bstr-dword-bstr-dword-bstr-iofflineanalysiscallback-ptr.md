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
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest:: RequestOfflineAnalysisAsync (método)

Solicita que se ejecute el análisis sin conexión con el origen especificado, el manifiesto, los parámetros y el marco especificado.

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
Especifica donde el origen del análisis procede de los informes almacenados en caché o de la reproducción.

*manifestXml*   
Cadena COM que contiene la ruta de acceso del archivo de manifiesto XML.

*parametersXml*   
Cadena COM que contiene la ruta de acceso del archivo de parámetros XML.

*ellas*   
Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.

*captureFullFileName*   
Cadena COM que contiene la ruta de acceso absoluta del archivo de captura (. vsglog).

*Númeromarco*   
Marco especificado.

*outputFullFileName*   
Cadena COM que contiene la ruta de acceso absoluta del archivo donde se escribe la salida.

*requestCallback*   
La dirección de una devolución de llamada que se utiliza para notificar al host los resultados.

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
