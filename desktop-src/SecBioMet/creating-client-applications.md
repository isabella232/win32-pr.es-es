---
title: Crear aplicaciones cliente
description: Cómo usar la API de Plataforma de biometría de Windows para crear aplicaciones cliente.
ms.assetid: 7bef37ee-7685-4aaa-8dad-3c5a9c335eca
keywords:
- API Plataforma de biometría de Windows API de Plataforma de biometría de Windows, aplicaciones cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c2b25df11897a4e5f164c079dc2cd31faa4e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685598"
---
# <a name="create-client-applications"></a><span data-ttu-id="aff78-104">Crear aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="aff78-104">Create client applications</span></span>

<span data-ttu-id="aff78-105">En los temas siguientes se explica cómo usar la API de Plataforma de biometría de Windows para crear aplicaciones cliente que usen grupos de sensores privados.</span><span class="sxs-lookup"><span data-stu-id="aff78-105">The following topics discuss how to use the Windows Biometric Framework API to create client applications that use private sensor pools.</span></span>

## <a name="enroll-biometric-information"></a><span data-ttu-id="aff78-106">Inscripción de información biométrica</span><span class="sxs-lookup"><span data-stu-id="aff78-106">Enroll biometric information</span></span>

<span data-ttu-id="aff78-107">En los siguientes ejemplos de código se muestra cómo inscribir una plantilla biométrica en el grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-107">The following code examples show how to enroll a biometric template in the system pool.</span></span>

### <a name="synchronous-enrollment"></a><span data-ttu-id="aff78-108">Inscripción sincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-108">Synchronous enrollment</span></span>

<span data-ttu-id="aff78-109">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-109">The following code example:</span></span>

-   <span data-ttu-id="aff78-110">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-110">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-111">Llama a [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) para buscar una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="aff78-111">Calls [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) to locate a biometric unit.</span></span>
-   <span data-ttu-id="aff78-112">Llama a [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) para iniciar la secuencia de inscripción.</span><span class="sxs-lookup"><span data-stu-id="aff78-112">Calls [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) to start the enrollment sequence.</span></span>
-   <span data-ttu-id="aff78-113">Llama a [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture) para procesar varios deslizamientos de dedo en el sensor.</span><span class="sxs-lookup"><span data-stu-id="aff78-113">Calls [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture) to process multiple finger swipes on the sensor.</span></span>
-   <span data-ttu-id="aff78-114">Llama a [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) para guardar la plantilla en el almacén.</span><span class="sxs-lookup"><span data-stu-id="aff78-114">Calls [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) to save the template in the store.</span></span>

<span data-ttu-id="aff78-115">Para compilar este ejemplo, vincule a la biblioteca estática Winbio. lib e incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-115">To compile this sample, link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-116">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-116">Windows.h</span></span>
-   <span data-ttu-id="aff78-117">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-117">Stdio.h</span></span>
-   <span data-ttu-id="aff78-118">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-118">Conio.h</span></span>
-   <span data-ttu-id="aff78-119">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-119">Winbio.h</span></span>


```C++
HRESULT EnrollSysPool(
                      BOOL discardEnrollment, 
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    BOOLEAN isNewTemplate = TRUE;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate a sensor.
    wprintf_s(L"\n Swipe your finger on the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    wprintf_s(L"\n Starting enrollment sequence...\n");
    hr = WinBioEnrollBegin(
            sessionHandle,      // Handle to open biometric session
            subFactor,          // Finger to create template for
            unitId              // Biometric unit ID
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollBegin failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Capture enrollment information by swiping the sensor with
    // the finger identified by the subFactor argument in the 
    // WinBioEnrollBegin function.
    for (int swipeCount = 1;; ++swipeCount)
    {
        wprintf_s(L"\n Swipe the sensor to capture %s sample.",
                 (swipeCount == 1)?L"the first":L"another");

        hr = WinBioEnrollCapture(
                sessionHandle,  // Handle to open biometric session
                &rejectDetail   // [out] Failure information
                );

        wprintf_s(L"\n Sample %d captured from unit number %d.", 
                  swipeCount, 
                  unitId);

        if (hr == WINBIO_I_MORE_DATA)
        {
            wprintf_s(L"\n    More data required.\n");
            continue;
        }
        if (FAILED(hr))
        {
            if (hr == WINBIO_E_BAD_CAPTURE)
            {
                wprintf_s(L"\n  Error: Bad capture; reason: %d", 
                          rejectDetail);
                continue;
            }
            else
            {
                wprintf_s(L"\n WinBioEnrollCapture failed. hr = 0x%x", hr);
                goto e_Exit;
            }
        }
        else
        {
            wprintf_s(L"\n    Template completed.\n");
            break;
        }
    }

    // Discard the enrollment if the appropriate flag is set.
    // Commit the enrollment if it is not discarded.
    if (discardEnrollment == TRUE)
    {
        wprintf_s(L"\n Discarding enrollment...\n\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &identity,          // WINBIO_IDENTITY object for the user
                &isNewTemplate);    // Is this a new template

        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioEnrollCommit failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }


e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L" Press any key to continue...");
    _getch();

    return hr;
}

```



### <a name="asynchronous-enrollment"></a><span data-ttu-id="aff78-120">Inscripción asincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-120">Asynchronous enrollment</span></span>

<span data-ttu-id="aff78-121">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-121">The following code example:</span></span>

-   <span data-ttu-id="aff78-122">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-122">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-123">Llama a [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) para buscar una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="aff78-123">Calls [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) to locate a biometric unit.</span></span>
-   <span data-ttu-id="aff78-124">Llama a [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) para iniciar la secuencia de inscripción.</span><span class="sxs-lookup"><span data-stu-id="aff78-124">Calls [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin) to start the enrollment sequence.</span></span>
-   <span data-ttu-id="aff78-125">Llama a [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) para procesar varios deslizadores de dedo.</span><span class="sxs-lookup"><span data-stu-id="aff78-125">Calls [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) to process multiple finger swipes.</span></span> <span data-ttu-id="aff78-126">Esta función es asincrónica y usa una función de devolución de llamada personalizada para continuar el procesamiento en un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="aff78-126">This function is asynchronous and uses a custom callback function to continue processing on a separate thread.</span></span> <span data-ttu-id="aff78-127">A continuación se incluye una función de devolución de llamada de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="aff78-127">An example callback function is included below.</span></span>
-   <span data-ttu-id="aff78-128">Llama a [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) para esperar a que se complete o se cancele el proceso de inscripción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="aff78-128">Calls [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) to wait for the asynchronous enrollment process to complete or be canceled.</span></span>
-   <span data-ttu-id="aff78-129">Llama a [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) para guardar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="aff78-129">Calls [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit) to save the template.</span></span>

<span data-ttu-id="aff78-130">Vínculo a la biblioteca estática Winbio. lib para compilar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="aff78-130">Link to the Winbio.lib static library to compile this sample.</span></span>


```C++
//------------------------------------------------------------------------
// EnrollSystemPoolWithCallback.cpp : Entry point for the application.
//
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <winbio.h>


//------------------------------------------------------------------------
// Forward declarations.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor);

VOID CALLBACK EnrollCaptureCallback(
                      __in_opt PVOID EnrollCallbackContext,
                      __in HRESULT OperationStatus,
                      __in WINBIO_REJECT_DETAIL RejectDetail);

typedef struct _ENROLL_CALLBACK_CONTEXT {
    WINBIO_SESSION_HANDLE SessionHandle;
    WINBIO_UNIT_ID UnitId;
    WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} ENROLL_CALLBACK_CONTEXT, *PENROLL_CALLBACK_CONTEXT;

//------------------------------------------------------------------------
int wmain()
{
    HRESULT hr = S_OK;

    hr = EnrollSysPoolWithCallback(
                      FALSE, 
                      FALSE, 
                      WINBIO_ANSI_381_POS_RH_INDEX_FINGER);

    return 0;
}

//------------------------------------------------------------------------
// The following function enrolls a user's fingerprint in the system pool.
// The function calls WinBioEnrollCaptureWithCallback and waits for the
// asynchronous enrollment process to be completed or canceled.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    BOOLEAN isNewTemplate = TRUE;
    ENROLL_CALLBACK_CONTEXT callbackContext = {0};

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the sensor.
    wprintf_s(L"\n Swipe your finger to locate the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    hr = WinBioEnrollBegin(
            sessionHandle,      // Handle to open biometric session
            subFactor,          // Finger to create template for
            unitId              // Biometric unit ID
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollBegin failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Set up the custom callback context structure.
    callbackContext.SessionHandle = sessionHandle;
    callbackContext.UnitId = unitId;
    callbackContext.SubFactor = subFactor;

    // Call WinBioEnrollCaptureWithCallback. This is an asynchronous
    // method that returns immediately.
    hr = WinBioEnrollCaptureWithCallback(
            sessionHandle,          // Handle to open biometric session
            EnrollCaptureCallback,  // Callback function
            &callbackContext        // Pointer to the custom context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollCaptureWithCallback failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor with the appropriate finger...\n");

    // Cancel the enrollment if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous enrollment process to complete
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

    // Discard the enrollment if the bDiscard flag is set.
    // Commit the enrollment if the flag is not set.
    if (bDiscard)
    {
        wprintf_s(L"\n Discarding enrollment...\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &identity,          // WINBIO_IDENTITY object for the user
                &isNewTemplate);    // Is this a new template

        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioEnrollCommit failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for the Windows Biometric
// Framework WinBioEnrollCaptureWithCallback() function. 
//
VOID CALLBACK EnrollCaptureCallback(
    __in_opt PVOID EnrollCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_REJECT_DETAIL RejectDetail
    )
{
    // Declare variables.
    HRESULT hr = S_OK; 
    static SIZE_T swipeCount = 1;

    PENROLL_CALLBACK_CONTEXT callbackContext = 
        (PENROLL_CALLBACK_CONTEXT)EnrollCallbackContext;

    wprintf_s(L"\n EnrollCaptureCallback executing\n");
    wprintf_s(L"\n Sample %d captured", swipeCount++);

    // The capture was not acceptable or the enrollment operation
    // failed.
    if (FAILED(OperationStatus))
    {
        if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
            wprintf_s(L"\n Swipe your finger to capture another sample.\n");

            // Try again.
            hr = WinBioEnrollCaptureWithCallback(
                    callbackContext->SessionHandle, // Open session handle
                    EnrollCaptureCallback,          // Callback function
                    EnrollCallbackContext           // Callback context
                    );
            if (FAILED(hr))
            {
                wprintf_s(L"WinBioEnrollCaptureWithCallback failed.");
                wprintf_s(L"hr = 0x%x\n", hr);
            }
        }
        else
        {
            wprintf_s(L"EnrollCaptureCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus);
        }
        goto e_Exit;
    }

    // The enrollment operation requires more fingerprint swipes.
    // This is normal and depends on your hardware. Typically, at least
    // three swipes are required.
    if (OperationStatus == WINBIO_I_MORE_DATA)
    {
        wprintf_s(L"\n More data required.");
        wprintf_s(L"\n Swipe your finger on the sensor again.");

        hr = WinBioEnrollCaptureWithCallback(
                callbackContext->SessionHandle,
                EnrollCaptureCallback,
                EnrollCallbackContext
                );
        if (FAILED(hr))
        {
            wprintf_s(L"WinBioEnrollCaptureWithCallback failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }

    wprintf_s(L"\n Template completed\n");

e_Exit:

    return;
}

```



## <a name="locate-biometric-units"></a><span data-ttu-id="aff78-131">Buscar unidades biométricas</span><span class="sxs-lookup"><span data-stu-id="aff78-131">Locate biometric units</span></span>

<span data-ttu-id="aff78-132">En los siguientes ejemplos de código se muestra cómo buscar una unidad biométrica instalada.</span><span class="sxs-lookup"><span data-stu-id="aff78-132">The following code examples show how to locate an installed biometric unit.</span></span>

### <a name="locate-biometric-units-synchronously"></a><span data-ttu-id="aff78-133">Buscar unidades biométricas de forma sincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-133">Locate biometric units synchronously</span></span>

<span data-ttu-id="aff78-134">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-134">The following code example:</span></span>

-   <span data-ttu-id="aff78-135">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-135">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-136">Llama a [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) para buscar una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="aff78-136">Calls [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor) to locate a biometric unit.</span></span>

<span data-ttu-id="aff78-137">Para compilar este ejemplo, vincule a la biblioteca estática Winbio. lib e incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-137">To compile this sample, link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-138">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-138">Windows.h</span></span>
-   <span data-ttu-id="aff78-139">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-139">Stdio.h</span></span>
-   <span data-ttu-id="aff78-140">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-140">Conio.h</span></span>
-   <span data-ttu-id="aff78-141">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-141">Winbio.h</span></span>


```C++
HRESULT LocateSensor( )
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the sensor.
    wprintf_s(L"\n Tap the sensor once...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Sensor located successfully. ");
    wprintf_s(L"\n Unit ID = %d \n", unitId);

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to exit...");
    _getch();

    return hr;
}

```



### <a name="locate-biometric-units-asynchronously"></a><span data-ttu-id="aff78-142">Buscar unidades biométricas de forma asincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-142">Locate biometric units asynchronously</span></span>

<span data-ttu-id="aff78-143">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-143">The following code example:</span></span>

-   <span data-ttu-id="aff78-144">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-144">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-145">Llama a [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) para buscar un sensor biométrico.</span><span class="sxs-lookup"><span data-stu-id="aff78-145">Calls [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) to locate a biometric sensor.</span></span> <span data-ttu-id="aff78-146">Se trata de una función asincrónica que configura el subsistema biométrico para ubicar el sensor en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="aff78-146">This is an asynchronous function that configures the biometric subsystem to locate the sensor on another thread.</span></span> <span data-ttu-id="aff78-147">La salida del subsistema biométrico se envía a una función de devolución de llamada personalizada, aquí denominada LocateSensorCallback.</span><span class="sxs-lookup"><span data-stu-id="aff78-147">Output from the biometric subsystem is sent to a custom callback function, here called LocateSensorCallback.</span></span>
-   <span data-ttu-id="aff78-148">Llama a [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) para esperar a que el proceso asincrónico se complete o se cancele.</span><span class="sxs-lookup"><span data-stu-id="aff78-148">Calls [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) to wait for the asynchronous process to complete or be canceled.</span></span>

<span data-ttu-id="aff78-149">Para compilar este ejemplo, vincule a la biblioteca estática Winbio. lib e incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-149">To compile this sample, link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-150">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-150">Windows.h</span></span>
-   <span data-ttu-id="aff78-151">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-151">Stdio.h</span></span>
-   <span data-ttu-id="aff78-152">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-152">Conio.h</span></span>
-   <span data-ttu-id="aff78-153">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-153">Winbio.h</span></span>


```C++
HRESULT LocateSensorWithCallback(BOOL bCancel)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    wprintf_s(L"\n Calling WinBioLocateSensorWithCallback.");
    hr = WinBioLocateSensorWithCallback(
                sessionHandle,          // Open biometric session
                LocateSensorCallback,   // Callback function
                NULL                    // Optional context
                );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensorWithCallback failed.");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous identification process to complete 
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

e_Exit:

    if (sessionHandle != NULL)
    {
       wprintf_s(L"\n Closing the session.\n");

        hr = WinBioCloseSession(sessionHandle);
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCloseSession failed. hr = 0x%x\n", hr);
        }
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for 
// WinBioLocateSensorWithCallback. The function filters the response 
// from the biometric subsystem and writes a result to the console window.
// 
VOID CALLBACK LocateSensorCallback(
    __in_opt PVOID LocateCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_UNIT_ID UnitId
    )
{
    UNREFERENCED_PARAMETER(LocateCallbackContext);

    wprintf_s(L"\n LocateSensorCallback executing.");

    // A sensor could not be located.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n LocateSensorCallback failed.");
        wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus);
    }
    // A sensor was located.
    else
    {
        wprintf_s(L"\n Selected unit ID: %d\n", UnitId);
    }
}

```



## <a name="verify-user-identity"></a><span data-ttu-id="aff78-154">Comprobar la identidad del usuario</span><span class="sxs-lookup"><span data-stu-id="aff78-154">Verify user identity</span></span>

### <a name="synchronous-verification"></a><span data-ttu-id="aff78-155">Comprobación sincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-155">Synchronous verification</span></span>

<span data-ttu-id="aff78-156">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-156">The following code example:</span></span>

-   <span data-ttu-id="aff78-157">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-157">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-158">Llama a [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify) para determinar si un ejemplo biométrico coincide con la identidad que inició la sesión del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="aff78-158">Calls [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify) to determine whether a biometric sample matches the logged on identity of the current user.</span></span>

<span data-ttu-id="aff78-159">Para compilar este ejemplo, vincule a la biblioteca estática Winbio. lib e incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-159">To compile this sample, link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-160">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-160">Windows.h</span></span>
-   <span data-ttu-id="aff78-161">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-161">Stdio.h</span></span>
-   <span data-ttu-id="aff78-162">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-162">Conio.h</span></span>
-   <span data-ttu-id="aff78-163">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-163">Winbio.h</span></span>


```C++
HRESULT Verify(WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_IDENTITY identity = {0};
    BOOLEAN match = FALSE;

    // Find the identity of the user.
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Verify a biometric sample.
    wprintf_s(L"\n Calling WinBioVerify - Swipe finger on sensor...\n");
    hr = WinBioVerify( 
            sessionHandle, 
            &identity, 
            subFactor, 
            &unitId, 
            &match,
            &rejectDetail
            );
    wprintf_s(L"\n Swipe processed - Unit ID: %d\n", unitId);
    if (FAILED(hr))
    {
        if (hr == WINBIO_E_NO_MATCH)
        {
            wprintf_s(L"\n- NO MATCH - identity verification failed.\n");
        }
        else if (hr == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n- Bad capture; reason: %d\n", rejectDetail);
        }
        else
        {
        wprintf_s(L"\n WinBioVerify failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }
    wprintf_s(L"\n Fingerprint verified:\n", unitId);


e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



### <a name="asynchronous-verification"></a><span data-ttu-id="aff78-164">Comprobación asincrónica</span><span class="sxs-lookup"><span data-stu-id="aff78-164">Asynchronous verification</span></span>

<span data-ttu-id="aff78-165">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-165">The following code example:</span></span>

-   <span data-ttu-id="aff78-166">Llama a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para abrir una sesión biométrica y conectarse al grupo del sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-166">Calls [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to open a biometric session and connect to the system pool.</span></span>
-   <span data-ttu-id="aff78-167">Llama a [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) para determinar si un ejemplo biométrico coincide con la identidad que inició la sesión del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="aff78-167">Calls [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) to determine whether a biometric sample matches the logged on identity of the current user.</span></span> <span data-ttu-id="aff78-168">Se trata de una función asincrónica que configura el subsistema biométrico para comprobar el usuario en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="aff78-168">This is an asynchronous function that configures the biometric subsystem to verify the user on another thread.</span></span> <span data-ttu-id="aff78-169">La salida del subsistema biométrico se envía a una función de devolución de llamada personalizada, aquí denominada VerifyCallback.</span><span class="sxs-lookup"><span data-stu-id="aff78-169">Output from the biometric subsystem is sent to a custom callback function, here called VerifyCallback.</span></span>
-   <span data-ttu-id="aff78-170">Llama a [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) para esperar a que el proceso asincrónico se complete o se cancele.</span><span class="sxs-lookup"><span data-stu-id="aff78-170">Calls [**WinBioWait**](/windows/desktop/api/Winbio/nf-winbio-winbiowait) to wait for the asynchronous process to complete or be canceled.</span></span>

<span data-ttu-id="aff78-171">Para compilar este ejemplo, vincule a la biblioteca estática Winbio. lib e incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-171">To compile this sample, link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-172">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-172">Windows.h</span></span>
-   <span data-ttu-id="aff78-173">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-173">Stdio.h</span></span>
-   <span data-ttu-id="aff78-174">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-174">Conio.h</span></span>
-   <span data-ttu-id="aff78-175">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-175">Winbio.h</span></span>


```C++
HRESULT VerifyWithCallback(BOOL bCancel, WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_IDENTITY identity = {0};

    // Find the identity of the user.
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Verify a biometric sample asynchronously.
    wprintf_s(L"\n Calling WinBioVerifyWithCallback.\n");
    hr = WinBioVerifyWithCallback(
            sessionHandle,              // Open session handle
            &identity,                  // User SID or GUID
            subFactor,                  // Sample sub-factor
            VerifyCallback,             // Callback function
            NULL                        // Optional context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioVerifyWithCallback failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous identification process to complete 
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to continue...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for WinBioVerifyWithCallback.
// The function filters the response from the biometric subsystem and 
// writes a result to the console window.
// 
VOID CALLBACK VerifyCallback(
  __in_opt PVOID VerifyCallbackContext,
  __in HRESULT OperationStatus,
  __in WINBIO_UNIT_ID UnitId,
  __in BOOLEAN Match,
  __in WINBIO_REJECT_DETAIL RejectDetail
  )
{
    UNREFERENCED_PARAMETER(VerifyCallbackContext);
    UNREFERENCED_PARAMETER(Match);

    wprintf_s(L"\n VerifyCallback executing");
    wprintf_s(L"\n Swipe processed for unit ID %d\n", UnitId);

    // The identity could not be verified.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n Verification failed for the following reason:");
        if (OperationStatus == WINBIO_E_NO_MATCH)
        {
            wprintf_s(L"\n No match.\n");
        }
        else if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture.\n ");
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
        }
        else
        {
            wprintf_s(L"VerifyCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus); 
        }
        goto e_Exit;
    }

    // The user identity was verified.
    wprintf_s(L"\n Fingerprint verified:\n");

e_Exit:
    return;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



## <a name="manage-credentials"></a><span data-ttu-id="aff78-176">Administración de credenciales</span><span class="sxs-lookup"><span data-stu-id="aff78-176">Manage credentials</span></span>

<span data-ttu-id="aff78-177">El proveedor de credenciales y el administrador de credenciales son componentes en el Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="aff78-177">The credential provider and the credential manager are components in the Windows Biometric Framework.</span></span> <span data-ttu-id="aff78-178">El proveedor recupera las credenciales del usuario del almacén seguro y responde a las solicitudes de elevación de inicio de sesión, desbloqueo, cambio de contraseña y elevación de UAC.</span><span class="sxs-lookup"><span data-stu-id="aff78-178">The provider retrieves user credentials from the secure store and responds to logon, unlock, password change, and UAC elevation requests.</span></span> <span data-ttu-id="aff78-179">También responde durante un cambio rápido de usuario para iniciar sesión del nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="aff78-179">It also responds during a fast user switch to logon the new user.</span></span> <span data-ttu-id="aff78-180">El administrador asigna las credenciales de inicio de sesión a las identidades biométricas y almacena las credenciales de forma segura.</span><span class="sxs-lookup"><span data-stu-id="aff78-180">The manager maps logon credentials to biometric identities and securely stores the credentials.</span></span> <span data-ttu-id="aff78-181">Las asignaciones suelen ser creadas por aplicaciones de inscripción de terceros durante la inscripción biométrica, pero también se pueden crear mediante el proveedor de credenciales biométricas de Windows durante el inicio de sesión si el usuario inscrito intenta autenticar biométricamente pero no está inscrito, o las credenciales no coinciden con las del almacén seguro.</span><span class="sxs-lookup"><span data-stu-id="aff78-181">Mappings are typically created by third party enrollment applications during biometric enrollment, but they can also be created by the Windows biometric credential provider during logon if the enrolled user attempts to authenticate biometrically but is either not enrolled or the credentials do not match those in the secure store.</span></span>

### <a name="credential-manager-api-guidelines"></a><span data-ttu-id="aff78-182">Directrices de API del administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="aff78-182">Credential Manager API Guidelines</span></span>

-   <span data-ttu-id="aff78-183">Las credenciales no se pueden almacenar, consultar ni eliminar para las cuentas de administrador invitado o integrado o para cualquier cuenta no interactiva, como LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="aff78-183">Credentials cannot be stored, queried, or deleted for the Guest or Built-in Administrator accounts or any non-interactive accounts such as LocalSystem, LocalService, or NetworkService.</span></span>
-   <span data-ttu-id="aff78-184">Todas las funciones devuelven un código de error **HRESULT** que puede ser un código de error común, como **E \_ ACCESSDENIED** , o un error específico del administrador de credenciales como **WINBIO \_ E \_ \_ identificador desconocido**.</span><span class="sxs-lookup"><span data-stu-id="aff78-184">All functions return an **HRESULT** error code that may be a common error code such as **E\_ACCESSDENIED** or an error specific to the credential manager such as **WINBIO\_E\_UNKNOWN\_ID**.</span></span>
-   <span data-ttu-id="aff78-185">Si es necesario, \_ se devuelve E ACCESSDENIED antes de que se devuelvan códigos de error más específicos, como sec \_ e \_ Logon \_ denegated o WINBIO \_ E \_ Unknown \_ ID.</span><span class="sxs-lookup"><span data-stu-id="aff78-185">If appropriate, E\_ACCESSDENIED is returned before more specific error codes such as SEC\_E\_LOGON\_DENIED or WINBIO\_E\_UNKNOWN\_ID are returned.</span></span>
-   <span data-ttu-id="aff78-186">Los usuarios cuyos privilegios no se hayan elevado pueden establecer, consultar o quitar credenciales solo para su propia cuenta.</span><span class="sxs-lookup"><span data-stu-id="aff78-186">Users whose privileges have not been elevated can set, query, or remove credentials for only their own account.</span></span> <span data-ttu-id="aff78-187">Los llamadores elevados pueden consultar el estado de las credenciales y quitar las credenciales de otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="aff78-187">Elevated callers can query credential state and remove credentials for other users.</span></span>
-   <span data-ttu-id="aff78-188">Se producirá un error en todas las funciones y se devolverá WINBIO \_ e \_ CRED \_ Prov \_ Disabled:</span><span class="sxs-lookup"><span data-stu-id="aff78-188">All functions will fail and return WINBIO\_E\_CRED\_PROV\_DISABLED:</span></span>
    -   <span data-ttu-id="aff78-189">Para todos los usuarios cuando el proveedor de credenciales no está habilitado para todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="aff78-189">For all users when the credential provider is not enabled system wide.</span></span>
    -   <span data-ttu-id="aff78-190">Para los usuarios del dominio cuando el proveedor no está habilitado para el uso del dominio.</span><span class="sxs-lookup"><span data-stu-id="aff78-190">For domain users when the provider is not enabled for domain use.</span></span>
-   <span data-ttu-id="aff78-191">Cuando se agrega o se quita una credencial, se genera un aviso de eventos.</span><span class="sxs-lookup"><span data-stu-id="aff78-191">An event notice is generated when a credential is added or removed.</span></span>

### <a name="set-a-credential"></a><span data-ttu-id="aff78-192">Establecer una credencial</span><span class="sxs-lookup"><span data-stu-id="aff78-192">Set a credential</span></span>

<span data-ttu-id="aff78-193">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-193">The following code example:</span></span>

-   <span data-ttu-id="aff78-194">Llama a GetCurrentUserIdentity para recuperar un objeto de [**\_ identidad WINBIO**](winbio-identity.md) para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="aff78-194">Calls GetCurrentUserIdentity to retrieve a [**WINBIO\_IDENTITY**](winbio-identity.md) object for the current user.</span></span> <span data-ttu-id="aff78-195">GetCurrentUserIdentity es una función auxiliar y no forma parte de la Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="aff78-195">GetCurrentUserIdentity is a helper function and is not part of the Windows Biometric Framework.</span></span>
-   <span data-ttu-id="aff78-196">Llama a la función auxiliar GetCredentials para recuperar una matriz de bytes que contiene información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="aff78-196">Calls the GetCredentials helper function to retrieve a byte array that contains authentication information.</span></span> <span data-ttu-id="aff78-197">GetCredentials muestra un cuadro de diálogo que solicita las credenciales al usuario.</span><span class="sxs-lookup"><span data-stu-id="aff78-197">GetCredentials displays a dialog box that prompts the user for credentials.</span></span>
-   <span data-ttu-id="aff78-198">Llama a [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) para guardar las credenciales en el almacén.</span><span class="sxs-lookup"><span data-stu-id="aff78-198">Calls [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) to save the credentials in the store.</span></span>

<span data-ttu-id="aff78-199">Para compilar este vínculo de función en la biblioteca estática Winbio. lib e incluir los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-199">To compile this function link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-200">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-200">Windows.h</span></span>
-   <span data-ttu-id="aff78-201">Wincred. h</span><span class="sxs-lookup"><span data-stu-id="aff78-201">Wincred.h</span></span>
-   <span data-ttu-id="aff78-202">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-202">Stdio.h</span></span>
-   <span data-ttu-id="aff78-203">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-203">Conio.h</span></span>
-   <span data-ttu-id="aff78-204">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-204">Winbio.h</span></span>


```C++
HRESULT SetCredential()
{
    // Declare variables.
    HRESULT hr = S_OK;
    ULONG   ulAuthPackage = 0;
    PVOID   pvAuthBlob = NULL;
    ULONG   cbAuthBlob = 0;
    WINBIO_IDENTITY identity;
    PSID pSid = NULL;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        return hr;
    }

    // Set a pointer to the security descriptor for the user.
    pSid = identity.Value.AccountSid.Data;

    // Retrieve a byte array that contains credential information.
    hr = GetCredentials(pSid, &pvAuthBlob, &cbAuthBlob);
    if (FAILED(hr))
    {
        wprintf_s(L"\n GetCredentials failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Set the credentials.
    hr = WinBioSetCredential(
            WINBIO_CREDENTIAL_PASSWORD,     // Type of credential.
            (PUCHAR)pvAuthBlob,             // Credentials byte array
            cbAuthBlob,                     // Size of credentials
            WINBIO_PASSWORD_PACKED);        // Credentials format

    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioSetCredential failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Credentials successfully set.\n");

e_Exit:
    // Delete the authentication byte array.
    if (NULL != pvAuthBlob)
    {
        SecureZeroMemory(pvAuthBlob, cbAuthBlob);
        CoTaskMemFree(pvAuthBlob);
        pvAuthBlob = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;


}

//------------------------------------------------------------------------
// The following function displays a dialog box to prompt a user
// for credentials.
//
HRESULT GetCredentials(PSID pSid, PVOID* ppvAuthBlob, ULONG* pcbAuthBlob)
{
    HRESULT hr = S_OK;
    DWORD   dwResult;
    WCHAR   szUsername[MAX_PATH] = {0};
    DWORD   cchUsername = ARRAYSIZE(szUsername);
    WCHAR   szPassword[MAX_PATH] = {0};
    WCHAR   szDomain[MAX_PATH] = {0};
    DWORD   cchDomain = ARRAYSIZE(szDomain);
    WCHAR   szDomainAndUser[MAX_PATH] = {0};
    DWORD   cchDomainAndUser = ARRAYSIZE(szDomainAndUser);
    PVOID   pvInAuthBlob = NULL;
    ULONG   cbInAuthBlob = 0;
    PVOID   pvAuthBlob = NULL;
    ULONG   cbAuthBlob = 0;
    CREDUI_INFOW ui;
    ULONG   ulAuthPackage = 0;
    BOOL    fSave = FALSE;

    static const WCHAR WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_MESSAGE[] =
           L"Enter your current password to enable biometric logon.";

    static const WCHAR WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_CAPTION[] =
           L"Biometric Log On Enrollment";

    if (NULL == pSid || NULL == ppvAuthBlob || NULL == pcbAuthBlob)
    {
        return E_INVALIDARG;
    }

    // Retrieve the user name and domain name.
    SID_NAME_USE    SidUse;
    DWORD           cchTmpUsername = cchUsername;
    DWORD           cchTmpDomain = cchDomain;

    if (!LookupAccountSidW(
              NULL,             // Local computer
              pSid,             // Security identifier for user
              szUsername,       // User name
              &cchTmpUsername,  // Size of user name
              szDomain,         // Domain name
              &cchTmpDomain,    // Size of domain name
              &SidUse))         // Account type
    {
        dwResult = GetLastError();
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n LookupAccountSidLocalW failed: hr = 0x%x\n", hr);
        return hr;
    }

    // Combine the domain and user names.
    swprintf_s(
        szDomainAndUser, 
        cchDomainAndUser, 
        L"%s\\%s", 
        szDomain, 
        szUsername);

    // Call CredPackAuthenticationBufferW once to determine the size,
    // in bytes, of the authentication buffer.
    if (!CredPackAuthenticationBufferW(
              0,                // Reserved
              szDomainAndUser,  // Domain\User name
              szPassword,       // User Password
              NULL,             // Packed credentials
              &cbInAuthBlob)    // Size, in bytes, of credentials
        && GetLastError() != ERROR_INSUFFICIENT_BUFFER)
        {
            dwResult = GetLastError();
            hr = HRESULT_FROM_WIN32(dwResult);
            wprintf_s(L"\n CredPackAuthenticationBufferW (1) failed: ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }

    // Allocate memory for the input buffer.
    pvInAuthBlob = CoTaskMemAlloc(cbInAuthBlob);
    if (!pvInAuthBlob)
    {
        cbInAuthBlob = 0;
        wprintf_s(L"\n CoTaskMemAlloc() Out of memory.\n");
        return HRESULT_FROM_WIN32(ERROR_OUTOFMEMORY);
    }

    // Call CredPackAuthenticationBufferW again to retrieve the
    // authentication buffer.
    if (!CredPackAuthenticationBufferW(
              0,
              szDomainAndUser,
              szPassword,
              (PBYTE)pvInAuthBlob,
              &cbInAuthBlob))
    {
        dwResult = GetLastError();
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n CredPackAuthenticationBufferW (2) failed: ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display a dialog box to request credentials.
    ui.cbSize = sizeof(ui);
    ui.hwndParent = GetConsoleWindow();
    ui.pszMessageText = WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_MESSAGE;
    ui.pszCaptionText = WINBIO_CREDPROV_TEST_PASSWORD_PROMPT_CAPTION;
    ui.hbmBanner = NULL;

    dwResult = CredUIPromptForWindowsCredentialsW(
                   &ui,             // Customizing information
                   0,               // Error code to display
                   &ulAuthPackage,  // Authorization package
                   pvInAuthBlob,    // Credential byte array
                   cbInAuthBlob,    // Size of credential input buffer
                   &pvAuthBlob,     // Output credential byte array
                   &cbAuthBlob,     // Size of credential byte array
                   &fSave,          // Select the save check box.
                   CREDUIWIN_IN_CRED_ONLY |
                   CREDUIWIN_ENUMERATE_CURRENT_USER
                   );
    if (dwResult != NO_ERROR)
    {
        hr = HRESULT_FROM_WIN32(dwResult);
        wprintf_s(L"\n CredUIPromptForWindowsCredentials failed: ");
        wprintf_s(L"0x%08x\n", dwResult);
        goto e_Exit;
    }

    *ppvAuthBlob = pvAuthBlob;
    *pcbAuthBlob = cbAuthBlob;

e_Exit:
    // Delete the input authentication byte array.
    if (pvInAuthBlob)
    {
        SecureZeroMemory(pvInAuthBlob, cbInAuthBlob);
        CoTaskMemFree(pvInAuthBlob);
        pvInAuthBlob = NULL;
    };

    return hr;
}


//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



### <a name="remove-a-credential"></a><span data-ttu-id="aff78-205">Quitar una credencial</span><span class="sxs-lookup"><span data-stu-id="aff78-205">Remove a credential</span></span>

<span data-ttu-id="aff78-206">En el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="aff78-206">The following code example:</span></span>

-   <span data-ttu-id="aff78-207">Llama a GetCurrentUserIdentity para recuperar un objeto de [**\_ identidad WINBIO**](winbio-identity.md) para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="aff78-207">Calls GetCurrentUserIdentity to retrieve a [**WINBIO\_IDENTITY**](winbio-identity.md) object for the current user.</span></span> <span data-ttu-id="aff78-208">GetCurrentUserIdentity es una función auxiliar y no forma parte de la Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="aff78-208">GetCurrentUserIdentity is a helper function and is not part of the Windows Biometric Framework.</span></span>
-   <span data-ttu-id="aff78-209">Llama a [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential) para eliminar las credenciales del almacén.</span><span class="sxs-lookup"><span data-stu-id="aff78-209">Calls [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential) to delete the credentials from the store.</span></span>

<span data-ttu-id="aff78-210">Para compilar este vínculo de función en la biblioteca estática Winbio. lib e incluir los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="aff78-210">To compile this function link to the Winbio.lib static library and include the following header files:</span></span>

-   <span data-ttu-id="aff78-211">Windows. h</span><span class="sxs-lookup"><span data-stu-id="aff78-211">Windows.h</span></span>
-   <span data-ttu-id="aff78-212">Stdio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-212">Stdio.h</span></span>
-   <span data-ttu-id="aff78-213">Conio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-213">Conio.h</span></span>
-   <span data-ttu-id="aff78-214">Winbio. h</span><span class="sxs-lookup"><span data-stu-id="aff78-214">Winbio.h</span></span>


```C++
HRESULT RemoveCredential()
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Remove the user credentials.
    hr = WinBioRemoveCredential(identity, WINBIO_CREDENTIAL_PASSWORD);
    if (FAILED(hr)) 
    {
        wprintf(L"\n WinBioRemoveCredential failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    wprintf_s(L"\n User credentials successfully removed.\n");

e_Exit:

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

```



 

 




