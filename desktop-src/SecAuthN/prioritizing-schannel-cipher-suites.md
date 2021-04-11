---
description: 'Cryptography API: Next Generation (CNG) proporciona funciones que consultan, agregan, quitan y priorizan los conjuntos de cifrado que admite un proveedor. Los cambios realizados mediante estas funciones surten efecto inmediatamente y no requieren reiniciar un servidor activo.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Dar prioridad a los conjuntos de cifrado Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279877"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Dar prioridad a los conjuntos de cifrado Schannel

[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) proporciona funciones que consultan, agregan, quitan y priorizan los conjuntos de cifrado que admite un proveedor. Los cambios realizados mediante estas funciones surten efecto inmediatamente y no requieren reiniciar un servidor activo.

> [!Note]
> También puede modificar la lista de conjuntos de cifrado mediante la configuración de las opciones de directiva de grupo del **orden de cifrado de SSL** mediante el complemento de directiva de grupo objeto en Microsoft Management Console.
> 
> **Para configurar la configuración de directiva de grupo de **orden de cifrado de SSL****
> 
> 1.  En un símbolo del sistema, escriba **gpedit. msc**. Aparece el **Editor de objetos de directiva de grupo** .
> 2.  Expanda **configuración del equipo**, **plantillas administrativas**, **red** y, a continuación, haga clic en configuración de **SSL**.
> 3.  En **configuración de SSL**, haga clic en la configuración **orden de conjunto de cifrado SSL** .
> 4.  En el panel **orden de conjunto de cifrado SSL** , desplácese a la parte inferior del panel.
> 5.  Siga las instrucciones etiquetadas **para modificar esta configuración**.
> 
> Es necesario reiniciar el equipo después de modificar esta configuración para que los cambios surtan efecto.

 

La lista de conjuntos de cifrado está limitada a 1023 caracteres.

Para dar prioridad a los conjuntos de cifrado Schannel, vea los ejemplos siguientes.

-   [Enumerar conjuntos de cifrado compatibles](#listing-supported-cipher-suites)
-   [Adición, eliminación y priorización de conjuntos de cifrado](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Enumerar conjuntos de cifrado compatibles

Llame a la función [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado que admite un proveedor por orden de prioridad.

En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado compatibles.


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Adición, eliminación y priorización de conjuntos de cifrado

Llame a las funciones [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) y [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para agregar y quitar conjuntos de cifrado de la lista de conjuntos de cifrado admitidos.

Al agregar un conjunto de cifrado, establezca el valor del parámetro *dwPosition* de la función [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) en la **prioridad de cifrado \_ \_ Top** para agregarlo a la parte superior de la lista con prioridad o para **cifrar la \_ prioridad \_ inferior** para agregarlo a la parte inferior de la lista.

Para dar prioridad a la lista de conjuntos de cifrado, quite todos los conjuntos de cifrado de la lista y, a continuación, agregue los conjuntos de cifrado a la lista en el orden que desee.

En el ejemplo siguiente se muestra cómo agregar un conjunto de cifrado a la parte superior de la lista de prioridades del proveedor de Microsoft Schannel predeterminado.


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



En el ejemplo siguiente se muestra cómo quitar un conjunto de cifrado de la lista con prioridad para el proveedor de Microsoft Schannel predeterminado.


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



 

 
