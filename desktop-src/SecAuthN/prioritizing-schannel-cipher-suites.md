---
description: 'Cryptography API: Next Generation (CNG) proporciona funciones que consultan, agregan, quitan y priorizan los conjuntos de cifrado que admite un proveedor. Los cambios realizados mediante estas funciones se hacen efectivos inmediatamente y no requieren reiniciar un servidor activo.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Priorización de conjuntos de cifrado de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920774"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Priorización de conjuntos de cifrado de Schannel

[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) proporciona funciones que consultan, agregan, quitan y priorizan los conjuntos de cifrado que admite un proveedor. Los cambios realizados mediante estas funciones se hacen efectivos inmediatamente y no requieren reiniciar un servidor activo.

> [!Note]
> También puede modificar la lista de conjuntos de cifrado mediante la configuración de la directiva de grupo Orden del conjunto de cifrado **SSL** mediante el complemento directiva de grupo Object en Microsoft Management Console.
> 
> **Para configurar la configuración **de la directiva de grupo Orden del conjunto** de cifrado SSL**
> 
> 1.  En un símbolo del sistema, escriba **gpedit.msc.** Aparece **el Editor de objetos de directiva de grupo.**
> 2.  Expanda **Configuración del** equipo , **Plantillas administrativas**, **Red** y, a continuación, haga clic en Configuración **ssl Configuración**.
> 3.  En **Configuración de SSL Configuración**, haga clic en la opción Orden del conjunto de **cifrado** SSL.
> 4.  En el **panel Orden del conjunto de cifrado SSL,** desplácese hasta la parte inferior del panel.
> 5.  Siga las instrucciones etiquetadas **como Modificación de esta configuración.**
> 
> Es necesario reiniciar el equipo después de modificar esta configuración para que los cambios sumen efecto.

 

La lista de conjuntos de cifrado está limitada a 1023 caracteres.

Para dar prioridad a los conjuntos de cifrado de Schannel, consulte los ejemplos siguientes.

-   [Enumeración de los conjuntos de cifrado admitidos](#listing-supported-cipher-suites)
-   [Agregar, quitar y priorizar conjuntos de cifrado](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Enumeración de los conjuntos de cifrado admitidos

Llame a [**la función BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado que admite un proveedor por orden de prioridad.

En el ejemplo siguiente se muestra cómo usar la [**función BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado admitidos.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Agregar, quitar y priorizar conjuntos de cifrado

Llame a [**las funciones BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) y [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para agregar y quitar conjuntos de cifrado de la lista de conjuntos de cifrado admitidos.

Al agregar un conjunto de cifrado, establezca el valor del parámetro *dwPosition* de la función [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) en **CRYPT \_ PRIORITY \_ TOP** para agregarlo a la parte superior de la lista con prioridad, o en **CRYPT \_ PRIORITY \_ BOTTOM** para agregarlo a la parte inferior de la lista.

Para priorizar la lista de conjuntos de cifrado, quite todos los conjuntos de cifrado de la lista y, a continuación, agregue los conjuntos de cifrado a la lista en el orden que desee.

En el ejemplo siguiente se muestra cómo agregar un conjunto de cifrado a la parte superior de la lista con prioridad para el proveedor de Microsoft Schannel predeterminado.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



En el ejemplo siguiente se muestra cómo quitar un conjunto de cifrado de la lista con prioridad para el proveedor predeterminado de Microsoft Schannel.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
