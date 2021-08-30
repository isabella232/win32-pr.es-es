---
description: Función de devolución de llamada que se usa para notificar al host que se ha completado el análisis sin conexión.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IOfflineAnalysisCallback::OfflineAnalysisComplete (método)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8829fbb94800a295f5e13ad2ec3c907c64fbfc93
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624151"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback::OfflineAnalysisComplete (método)

Función de devolución de llamada que se usa para notificar al host que se ha completado el análisis sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a>Parámetros

*Galleta*   
Cookie que identifica de forma única la solicitud que inició el análisis sin conexión.

*Resultado*   
Indica si el análisis sin conexión se ha realizado correctamente o no. Si se realiza correctamente, los resultados se escriben en un archivo.

*outputFullFileName*   
Cadena COM que contiene el nombre del archivo donde se escribieron los resultados del análisis sin conexión.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IOfflineAnalysisCallback**](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
