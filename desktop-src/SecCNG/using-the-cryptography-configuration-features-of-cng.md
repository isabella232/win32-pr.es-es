---
description: Proporciona funciones para enumerar y obtener información sobre los proveedores registrados.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Usar las características de configuración de criptografía de CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666495"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="360ac-103">Usar las características de configuración de criptografía de CNG</span><span class="sxs-lookup"><span data-stu-id="360ac-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="360ac-104">La API CNG proporciona funciones para enumerar y obtener información sobre los proveedores registrados.</span><span class="sxs-lookup"><span data-stu-id="360ac-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="360ac-105">Enumeración de proveedores</span><span class="sxs-lookup"><span data-stu-id="360ac-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="360ac-106">Obtención de información de registro del proveedor</span><span class="sxs-lookup"><span data-stu-id="360ac-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="360ac-107">Enumeración de proveedores</span><span class="sxs-lookup"><span data-stu-id="360ac-107">Enumerating Providers</span></span>

<span data-ttu-id="360ac-108">La función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) se usa para enumerar los proveedores registrados.</span><span class="sxs-lookup"><span data-stu-id="360ac-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="360ac-109">Se puede llamar a la función **BCryptEnumRegisteredProviders** de una de estas dos maneras:</span><span class="sxs-lookup"><span data-stu-id="360ac-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="360ac-110">La primera es hacer que la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) asigne la memoria.</span><span class="sxs-lookup"><span data-stu-id="360ac-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="360ac-111">Esto se logra pasando la dirección de un puntero **nulo** para el parámetro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="360ac-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="360ac-112">Este código asignará la memoria necesaria para la estructura de [**\_ proveedores de cifrado**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) y las cadenas asociadas.</span><span class="sxs-lookup"><span data-stu-id="360ac-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="360ac-113">Cuando la función **BCryptEnumRegisteredProviders** se usa de esta manera, debe liberar la memoria cuando ya no se necesite pasando *ppBuffer* a la función [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .</span><span class="sxs-lookup"><span data-stu-id="360ac-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="360ac-114">En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para asignar el búfer automáticamente.</span><span class="sxs-lookup"><span data-stu-id="360ac-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  <span data-ttu-id="360ac-115">El segundo método consiste en asignar la memoria necesaria.</span><span class="sxs-lookup"><span data-stu-id="360ac-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="360ac-116">Esto se logra mediante una llamada a la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) con **null** para el parámetro *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="360ac-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="360ac-117">La función **BCryptEnumRegisteredProviders** se colocará en el valor al que apunta el parámetro *pcbBuffer* , el tamaño requerido, en bytes, de la estructura de los [**\_ proveedores de cifrado**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) y todas las cadenas.</span><span class="sxs-lookup"><span data-stu-id="360ac-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="360ac-118">A continuación, asigne la memoria necesaria y pase la dirección de este puntero de búfer para el parámetro *ppBuffer* en una segunda llamada a la función **BCryptEnumRegisteredProviders** .</span><span class="sxs-lookup"><span data-stu-id="360ac-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="360ac-119">En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para asignar y usar su propio búfer.</span><span class="sxs-lookup"><span data-stu-id="360ac-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="360ac-120">Obtención de información de registro del proveedor</span><span class="sxs-lookup"><span data-stu-id="360ac-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="360ac-121">La función [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) se usa para obtener información adicional específica del registro sobre un proveedor.</span><span class="sxs-lookup"><span data-stu-id="360ac-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="360ac-122">Esta función toma el nombre del proveedor para el que desea obtener información, el modo de proveedor deseado (modo kernel, modo de usuario o ambos) y el identificador de la interfaz del proveedor para el que recuperar la información de registro.</span><span class="sxs-lookup"><span data-stu-id="360ac-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="360ac-123">Por ejemplo, para obtener la información de registro del modo de usuario para la interfaz de cifrado para el proveedor de "proveedor primitivo de Microsoft", realizaría una llamada similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="360ac-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="360ac-124">Al igual que la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la función [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) puede asignar memoria automáticamente o puede asignar la memoria usted mismo.</span><span class="sxs-lookup"><span data-stu-id="360ac-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="360ac-125">El proceso es el mismo para las dos funciones.</span><span class="sxs-lookup"><span data-stu-id="360ac-125">The process is the same for the two functions.</span></span>

 

 



