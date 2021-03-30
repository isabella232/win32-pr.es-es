---
description: Se ha creado una instancia del control de inscripción de certificados en C++
ms.assetid: 19dd2fce-b4a9-44fd-9572-897ee7943914
title: Se ha creado una instancia del control de inscripción de certificados en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 868f89e0a285460c587a924e84a5ed21c202eb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818979"
---
# <a name="the-certificate-enrollment-control-instantiated-in-c"></a>Se ha creado una instancia del control de inscripción de certificados en C++

En el siguiente ejemplo de C++ se inicializa COM, se crea una instancia del [control de inscripción de certificados](certificate-enrollment-control.md), se utiliza el control de inscripción de certificados y se liberan recursos.

## <a name="example-in-c"></a>Ejemplo en C++

En el ejemplo siguiente se crea una instancia del [control de inscripción de certificados](certificate-enrollment-control.md) y se muestra el valor de la propiedad [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) . En este ejemplo se usa la interfaz [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) .


```C++
#include <windows.h>
#include <stdio.h>
#include <xenroll.h>

// Copyright (C) Microsoft.  All rights reserved.
HRESULT __cdecl main(void)
{
    HRESULT hr = 0;
    ICEnroll4 *pEnroll = NULL;
    BSTR bstrStoreName = NULL;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [0x%x]\n", hr);
        exit(hr);
    }

    // Create an instance of the object.
    hr = CoCreateInstance( __uuidof(CEnroll),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(ICEnroll4),
                           (void **)&pEnroll);
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [0x%x]\n", hr);
        exit(hr);
    }

    hr = pEnroll->get_MyStoreName(&bstrStoreName);
    if (SUCCEEDED(hr))
    {
        printf("The value of MyStoreName is %ws\n", bstrStoreName);
    }
    else
    {
        printf("pEnroll->GetMyStoreName failed: 0x%x\n", hr);
    }

    pEnroll->Release();
    SysFreeString(bstrStoreName);
    CoUninitialize();

    return hr;
}
```



 

 
