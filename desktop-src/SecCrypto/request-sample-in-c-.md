---
description: En el ejemplo siguiente se muestra cómo se puede usar el control de inscripción de certificados con el objeto ICertRequest para crear y enviar una solicitud de certificado.
ms.assetid: 2816e1f8-c4be-4905-b070-6e67255811d4
title: Ejemplo de solicitud en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbcaea567ed6d6427ab17cf1b99c0a41807651
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476372"
---
# <a name="request-sample-in-c"></a>Ejemplo de solicitud en C++

En el ejemplo siguiente se muestra cómo se puede usar el control de inscripción de certificados con el [**objeto ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) para crear y enviar una solicitud de certificado.


```C++
// Copyright (C) Microsoft.  All rights reserved.
// Example for Certificate Enrollment Control
// used with ICertRequest in C++
// 

#include <stdio.h>
#include <Certsrv.h> // for ICertRequest object
#include <xenroll.h>
#include <windows.h>

HRESULT __cdecl main()
{

    // Pointer to interface objects.
    ICEnroll4 * pEnroll = NULL;
    ICertRequest2 * pRequest = NULL;

    // BSTR variables.
    BSTR    bstrDN = NULL;
    BSTR    bstrOID = NULL;
    BSTR    bstrCertAuth = NULL;
    BSTR    bstrReq = NULL;
    BSTR    bstrAttrib = NULL;

    // Request disposition variable.
    long    nDisp;

    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );

    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [%x]\n", hr);
        goto error;
    }

    // Create an instance of the Certificate Enrollment object.
    hr = CoCreateInstance( CLSID_CEnroll,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICEnroll4,
                           (void **)&pEnroll);
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
        goto error;
    }

    // Create an instance of the Certificate Request object.
    hr = CoCreateInstance( CLSID_CCertRequest,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertRequest2,
                           (void **)&pRequest);
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
        goto error;
    }

    // Create the data for the request.
    // A user interface or database retrieval could
    // be used instead of this sample's hard-coded text.
    bstrDN = SysAllocString(L"CN=UserName"    // Common Name
                            L",OU=UserUnit"   // Org Unit
                            L",O=UserOrg"     // Org
                            L",L=UserCity"    // Locality
                            L",S=WA"          // State
                            L",C=US");        // Country/Region
    if (NULL == bstrDN)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR representing the certification authority.
    // Note the use of '\\' to produce a single '\' in C++.
    bstrCertAuth = SysAllocString(L"Server\\CertAuth");
    if (NULL == bstrCertAuth)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR for the certificate usage.
    bstrOID = SysAllocString(L"1.3.6.1.4.1.311.2.1.21");
    if (NULL == bstrOID)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR for the attributes.
    // In this case, no attribute is specified.
    bstrAttrib = SysAllocString(L"");
    if (NULL == bstrAttrib)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Create the PKCS #10.
    hr = pEnroll->createPKCS10( bstrDN, bstrOID, &bstrReq );
    // check status
    if ( FAILED( hr ) )
    {
        printf("Failed createPKCS10 - [%x]\n", hr);
        goto error;
    }

    // Submit the certificate request.
    hr = pRequest->Submit( CR_IN_BASE64 | CR_IN_PKCS10,
                           bstrReq,
                           bstrAttrib,
                           bstrCertAuth,
                           &nDisp );
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed Request Submit - [%x]\n", hr);
        goto error;
    }
    else
        printf("Request submitted; disposition = %d\n", nDisp );

error:

    // Done processing.
    // Clean up object resources.
    if ( NULL != pEnroll )
        pEnroll->Release();
    if ( NULL != pRequest )
        pRequest->Release();

    // Free BSTR variables.
    if ( NULL != bstrDN )
        SysFreeString ( bstrDN );
    if ( NULL != bstrOID )
        SysFreeString ( bstrOID );
    if ( NULL != bstrCertAuth )
        SysFreeString ( bstrCertAuth );
    if ( NULL != bstrReq )
        SysFreeString ( bstrReq );
    if ( NULL != bstrAttrib )
        SysFreeString ( bstrAttrib );

    // Free COM resources.
    CoUninitialize();

    return hr;
}
```



 

 



