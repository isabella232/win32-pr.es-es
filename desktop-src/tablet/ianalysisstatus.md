---
description: Representa el estado de la operación de análisis de tinta al describir si el análisis se completó correctamente y si se produjo alguna advertencia.
ms.assetid: 57910a1d-3472-4689-ba0d-a220145e77c4
title: Interfaz IAnalysisStatus (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e14f7fabea8090f5471513eca524f6fcdb939b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154447"
---
# <a name="ianalysisstatus-interface"></a>Interfaz IAnalysisStatus

Representa el estado de la operación de análisis de tinta al describir si el análisis se completó correctamente y si se produjo alguna advertencia.

## <a name="members"></a>Miembros

La interfaz **IAnalysisStatus** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisStatus** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAnalysisStatus** tiene estos métodos.



| Método                                                                     | Descripción                                                                                                                                                                                    |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAppliedChangesRegion**](ianalysisstatus-getappliedchangesregion.md) | Recupera la región del documento correspondiente a los cambios que se realizaron en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado del análisis de tinta.<br/> |
| [**GetWarnings**](ianalysisstatus-getwarnings.md)                         | Recupera una colección [**IAnalysisWarnings**](ianalysiswarnings.md) que describe los errores y advertencias generados por la operación de análisis.<br/>                                  |
| [**IsSuccessful**](ianalysisstatus-issuccessful.md)                       | Recupera un resumen booleano de los resultados de la operación de análisis.<br/>                                                                                                               |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un esquema de un controlador de eventos para el evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) . El controlador comprueba [**IAnalysisStatus:: IsSuccessful**](ianalysisstatus-issuccessful.md). Si la operación de análisis genera advertencias, el controlador recorre en iteración la colección de objetos [**IAnalysisWarning**](ianalysiswarning.md) .


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer:: Analyze (método)**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer:: BackgroundAnalyze (método)**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

