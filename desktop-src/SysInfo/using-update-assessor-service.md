---
description: Para usar la API de waaS Assessment Platform, cree una instancia de la interfaz IWaaSAssessor y, a continuación, llame al método GetOSUpdateAssessment.
ms.assetid: 810D4057-8319-4B9B-9098-CD7987CB292C
title: Uso de la plataforma de evaluación de WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08401222b11036047a6c03e98cccaa9dc65e6f6a7cf39470480479c217549d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884246"
---
# <a name="using-the-waas-assessment-platform"></a>Uso de la plataforma de evaluación de WaaS

Para usar la API de waaS Assessment Platform, cree una instancia de la interfaz [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor) y, a continuación, llame al [**método GetOSUpdateAssessment.**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) Si se ejecuta correctamente, el *parámetro result* genera un [**objeto OSUpdateAssessment,**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) que contendrá la información pertinente.

En el ejemplo de código siguiente se muestra cómo recuperar una evaluación del sistema operativo del sistema local mediante el método IWaaSAssessor.GetOSUpdateAssessment.


```C++
//
// Copyright (c) Microsoft Corporation.  All rights reserved.
//
#include <windows.h>
#include <tchar.h>
#include <oaidl.h>
#include <atlbase.h>
#include <iostream>
#include <WaaSAPI.h>
#include <WaaSAPITypes.h>

using namespace std;

void __cdecl main(int argc, char** argv)
{
    HRESULT hr = S_OK;
    CComPtr<IWaaSAssessor> assessment;
    OSUpdateAssessment result;
    hr = CoInitialize(NULL);
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(
                __uuidof(WaaSAssessor),               // rclsid
                NULL,                                   // pUnkOuter
                CLSCTX_INPROC_SERVER,                   // dwClsContext
                __uuidof(IWaaSAssessor),              // riid
                (LPVOID*)&assessment);                  // ppv
        if (SUCCEEDED(hr))
        {
            hr = assessment->GetOSUpdateAssessment(&result);
            if (SUCCEEDED(hr))
            {
                wcout << L"End of Support:" << result.isEndOfSupport << endl;
                wcout << L"Up to date:" << result.assessmentForUpToDate.status << endl;
                wcout << L"Current:" << result.assessmentForCurrent.status << endl;
                wcout << L"Up to Date Days Behind:" << result.assessmentForUpToDate.daysOutOfDate << endl;
                wcout << L"Current Days Behind:" << result.assessmentForCurrent.daysOutOfDate << endl;
                wcout << L"Up to Date Impact:" << result.assessmentForUpToDate.impact << endl;
                wcout << L"Current Impact:" << result.assessmentForCurrent.impact << endl;
            }
            else
            {
                wcout << L"Assessment Failed hr = " << hr << endl;
            }
        }
        else
        {
            wcout << L"CoCreateInstance Failed hr = " << hr << endl;
        }
    }
    else
    {
        wcout << L"CoInitialize Failed hr = " << hr << endl;
    }
}
```



 

 



