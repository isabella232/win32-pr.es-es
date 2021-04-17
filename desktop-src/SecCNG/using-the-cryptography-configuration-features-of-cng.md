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
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Usar las características de configuración de criptografía de CNG

La API CNG proporciona funciones para enumerar y obtener información sobre los proveedores registrados.

-   [Enumeración de proveedores](#enumerating-providers)
-   [Obtención de información de registro del proveedor](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Enumeración de proveedores

La función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) se usa para enumerar los proveedores registrados. Se puede llamar a la función **BCryptEnumRegisteredProviders** de una de estas dos maneras:

1.  La primera es hacer que la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) asigne la memoria. Esto se logra pasando la dirección de un puntero **nulo** para el parámetro *ppBuffer* . Este código asignará la memoria necesaria para la estructura de [**\_ proveedores de cifrado**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) y las cadenas asociadas. Cuando la función **BCryptEnumRegisteredProviders** se usa de esta manera, debe liberar la memoria cuando ya no se necesite pasando *ppBuffer* a la función [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .

    En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para asignar el búfer automáticamente.

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

    

2.  El segundo método consiste en asignar la memoria necesaria. Esto se logra mediante una llamada a la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) con **null** para el parámetro *ppBuffer* . La función **BCryptEnumRegisteredProviders** se colocará en el valor al que apunta el parámetro *pcbBuffer* , el tamaño requerido, en bytes, de la estructura de los [**\_ proveedores de cifrado**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) y todas las cadenas. A continuación, asigne la memoria necesaria y pase la dirección de este puntero de búfer para el parámetro *ppBuffer* en una segunda llamada a la función **BCryptEnumRegisteredProviders** .

    En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) para asignar y usar su propio búfer.

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

    

## <a name="getting-provider-registration-information"></a>Obtención de información de registro del proveedor

La función [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) se usa para obtener información adicional específica del registro sobre un proveedor. Esta función toma el nombre del proveedor para el que desea obtener información, el modo de proveedor deseado (modo kernel, modo de usuario o ambos) y el identificador de la interfaz del proveedor para el que recuperar la información de registro. Por ejemplo, para obtener la información de registro del modo de usuario para la interfaz de cifrado para el proveedor de "proveedor primitivo de Microsoft", realizaría una llamada similar a la siguiente.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



Al igual que la función [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la función [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) puede asignar memoria automáticamente o puede asignar la memoria usted mismo. El proceso es el mismo para las dos funciones.

 

 



