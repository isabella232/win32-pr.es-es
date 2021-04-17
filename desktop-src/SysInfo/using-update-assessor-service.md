---
description: Para usar la API de la plataforma de evaluación de WaaS, cree una instancia de la interfaz IWaaSAssessor y, a continuación, llame al método GetOSUpdateAssessment.
ms.assetid: 810D4057-8319-4B9B-9098-CD7987CB292C
title: Uso de la plataforma de evaluación de WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3a7d70e3dab0c75aea266f2a1874931e5e5d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666928"
---
# <a name="using-the-waas-assessment-platform"></a><span data-ttu-id="efea5-103">Uso de la plataforma de evaluación de WaaS</span><span class="sxs-lookup"><span data-stu-id="efea5-103">Using the WaaS Assessment Platform</span></span>

<span data-ttu-id="efea5-104">Para usar la API de la plataforma de evaluación de WaaS, cree una instancia de la interfaz [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor) y, a continuación, llame al método [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) .</span><span class="sxs-lookup"><span data-stu-id="efea5-104">To use the WaaS Assessment Platform API, create an instance of the [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor) interface, and then call the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method.</span></span> <span data-ttu-id="efea5-105">Si se ejecuta correctamente, el parámetro de *resultado* generará un objeto [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , que contendrá la información pertinente.</span><span class="sxs-lookup"><span data-stu-id="efea5-105">On a success, the *result* parameter will output an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) object, which will contain the relevant information.</span></span>

<span data-ttu-id="efea5-106">En el ejemplo de código siguiente se muestra cómo recuperar una evaluación del sistema operativo desde el sistema local mediante el método IWaaSAssessor. GetOSUpdateAssessment.</span><span class="sxs-lookup"><span data-stu-id="efea5-106">The following code sample shows how to retrieve an OS assessment from your local system, using the IWaaSAssessor.GetOSUpdateAssessment method.</span></span>


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



 

 



