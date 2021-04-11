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
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="06736-104">Dar prioridad a los conjuntos de cifrado Schannel</span><span class="sxs-lookup"><span data-stu-id="06736-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="06736-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) proporciona funciones que consultan, agregan, quitan y priorizan los conjuntos de cifrado que admite un proveedor.</span><span class="sxs-lookup"><span data-stu-id="06736-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="06736-106">Los cambios realizados mediante estas funciones surten efecto inmediatamente y no requieren reiniciar un servidor activo.</span><span class="sxs-lookup"><span data-stu-id="06736-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="06736-107">También puede modificar la lista de conjuntos de cifrado mediante la configuración de las opciones de directiva de grupo del **orden de cifrado de SSL** mediante el complemento de directiva de grupo objeto en Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="06736-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="06736-108">\*\*Para configurar la configuración de directiva de grupo de \*\*orden de cifrado de SSL\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="06736-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="06736-109">En un símbolo del sistema, escriba **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="06736-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="06736-110">Aparece el **Editor de objetos de directiva de grupo** .</span><span class="sxs-lookup"><span data-stu-id="06736-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="06736-111">Expanda **configuración del equipo**, **plantillas administrativas**, **red** y, a continuación, haga clic en configuración de **SSL**.</span><span class="sxs-lookup"><span data-stu-id="06736-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="06736-112">En **configuración de SSL**, haga clic en la configuración **orden de conjunto de cifrado SSL** .</span><span class="sxs-lookup"><span data-stu-id="06736-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="06736-113">En el panel **orden de conjunto de cifrado SSL** , desplácese a la parte inferior del panel.</span><span class="sxs-lookup"><span data-stu-id="06736-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="06736-114">Siga las instrucciones etiquetadas **para modificar esta configuración**.</span><span class="sxs-lookup"><span data-stu-id="06736-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="06736-115">Es necesario reiniciar el equipo después de modificar esta configuración para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="06736-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="06736-116">La lista de conjuntos de cifrado está limitada a 1023 caracteres.</span><span class="sxs-lookup"><span data-stu-id="06736-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="06736-117">Para dar prioridad a los conjuntos de cifrado Schannel, vea los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="06736-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="06736-118">Enumerar conjuntos de cifrado compatibles</span><span class="sxs-lookup"><span data-stu-id="06736-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="06736-119">Adición, eliminación y priorización de conjuntos de cifrado</span><span class="sxs-lookup"><span data-stu-id="06736-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="06736-120">Enumerar conjuntos de cifrado compatibles</span><span class="sxs-lookup"><span data-stu-id="06736-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="06736-121">Llame a la función [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado que admite un proveedor por orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="06736-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="06736-122">En el ejemplo siguiente se muestra cómo usar la función [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) para enumerar los conjuntos de cifrado compatibles.</span><span class="sxs-lookup"><span data-stu-id="06736-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="06736-123">Adición, eliminación y priorización de conjuntos de cifrado</span><span class="sxs-lookup"><span data-stu-id="06736-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="06736-124">Llame a las funciones [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) y [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) para agregar y quitar conjuntos de cifrado de la lista de conjuntos de cifrado admitidos.</span><span class="sxs-lookup"><span data-stu-id="06736-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="06736-125">Al agregar un conjunto de cifrado, establezca el valor del parámetro *dwPosition* de la función [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) en la **prioridad de cifrado \_ \_ Top** para agregarlo a la parte superior de la lista con prioridad o para **cifrar la \_ prioridad \_ inferior** para agregarlo a la parte inferior de la lista.</span><span class="sxs-lookup"><span data-stu-id="06736-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="06736-126">Para dar prioridad a la lista de conjuntos de cifrado, quite todos los conjuntos de cifrado de la lista y, a continuación, agregue los conjuntos de cifrado a la lista en el orden que desee.</span><span class="sxs-lookup"><span data-stu-id="06736-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="06736-127">En el ejemplo siguiente se muestra cómo agregar un conjunto de cifrado a la parte superior de la lista de prioridades del proveedor de Microsoft Schannel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="06736-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



<span data-ttu-id="06736-128">En el ejemplo siguiente se muestra cómo quitar un conjunto de cifrado de la lista con prioridad para el proveedor de Microsoft Schannel predeterminado.</span><span class="sxs-lookup"><span data-stu-id="06736-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



 

 
