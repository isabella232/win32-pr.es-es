---
description: La contraseña de inicio de sesión automática debe protegerse mediante la función LsaStorePrivateData.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Protección de la contraseña de inicio de sesión automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25508af4de64554e664426db3e786a1eca34579b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002689"
---
# <a name="protecting-the-automatic-logon-password"></a><span data-ttu-id="28b37-103">Protección de la contraseña de inicio de sesión automático</span><span class="sxs-lookup"><span data-stu-id="28b37-103">Protecting the Automatic Logon Password</span></span>

<span data-ttu-id="28b37-104">La contraseña de inicio de sesión automática debe protegerse mediante la función [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="28b37-104">The automatic logon password should be protected by using the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span>

<span data-ttu-id="28b37-105">En el ejemplo siguiente se muestra cómo proteger la contraseña de inicio de sesión automático.</span><span class="sxs-lookup"><span data-stu-id="28b37-105">The following example shows how to protect the automatic logon password.</span></span> <span data-ttu-id="28b37-106">En el ejemplo se recupera un identificador para el objeto de [**Directiva**](../secmgmt/policy-object.md) mediante una llamada a la función [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) .</span><span class="sxs-lookup"><span data-stu-id="28b37-106">The example retrieves a handle to the [**Policy**](../secmgmt/policy-object.md) object by calling the [**LsaOpenPolicy**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) function.</span></span> <span data-ttu-id="28b37-107">Para obtener más información sobre el objeto de **Directiva** y los identificadores de objetos de **Directiva** **, vea objeto de directiva y** [abrir un identificador de objeto de directiva](../secmgmt/opening-a-policy-object-handle.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="28b37-107">For more information about the **Policy** object and **Policy** object handles, see **Policy** object and [Opening a Policy Object Handle](../secmgmt/opening-a-policy-object-handle.md), respectively.</span></span> <span data-ttu-id="28b37-108">A continuación, en el ejemplo se establece la contraseña protegida mediante una llamada a la función [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="28b37-108">The example then sets the protected password by calling the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function.</span></span> <span data-ttu-id="28b37-109">Tenga en cuenta que si el autor de la llamada pasa **null** para el valor de contraseña protegida, el código borra la contraseña protegida existente.</span><span class="sxs-lookup"><span data-stu-id="28b37-109">Note that if the caller passes in **NULL** for the protected password value, then the code clears the existing protected password.</span></span> <span data-ttu-id="28b37-110">Antes de salir, el código cierra el identificador del objeto de **Directiva** .</span><span class="sxs-lookup"><span data-stu-id="28b37-110">Before exiting, the code closes the handle to the **Policy** object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD UpdateDefaultPassword(WCHAR * pwszSecret)
{

    LSA_OBJECT_ATTRIBUTES ObjectAttributes;
    LSA_HANDLE LsaPolicyHandle = NULL;

    LSA_UNICODE_STRING lusSecretName;
    LSA_UNICODE_STRING lusSecretData;
    USHORT SecretNameLength;
    USHORT SecretDataLength;

    NTSTATUS ntsResult = STATUS_SUCCESS;
    DWORD dwRetCode = ERROR_SUCCESS;

    //  Object attributes are reserved, so initialize to zeros.
    ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

    //  Get a handle to the Policy object.
    ntsResult = LsaOpenPolicy(
        NULL,    // local machine
        &ObjectAttributes, 
        POLICY_CREATE_SECRET,
        &LsaPolicyHandle);

    if( STATUS_SUCCESS != ntsResult )
    {
        //  An error occurred. Display it as a win32 error code.
        dwRetCode = LsaNtStatusToWinError(ntsResult);
        wprintf(L"Failed call to LsaOpenPolicy %lu\n", dwRetCode);
        return dwRetCode;
    } 

    //  Initialize an LSA_UNICODE_STRING for the name of the
    //  private data ("DefaultPassword").
    SecretNameLength = (USHORT)wcslen(L"DefaultPassword");
    lusSecretName.Buffer = L"DefaultPassword";
    lusSecretName.Length = SecretNameLength * sizeof(WCHAR);
    lusSecretName.MaximumLength =
        (SecretNameLength+1) * sizeof(WCHAR);

    //  If the pwszSecret parameter is NULL, then clear the secret.
    if( NULL == pwszSecret )
    {
        wprintf(L"Clearing the secret...\n");
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            NULL);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }
    else
    {
        wprintf(L"Setting the secret...\n");
        //  Initialize an LSA_UNICODE_STRING for the value
        //  of the private data. 
        SecretDataLength = (USHORT)wcslen(pwszSecret);
        lusSecretData.Buffer = pwszSecret;
        lusSecretData.Length = SecretDataLength * sizeof(WCHAR);
        lusSecretData.MaximumLength =
            (SecretDataLength+1) * sizeof(WCHAR);
        ntsResult = LsaStorePrivateData(
            LsaPolicyHandle,
            &lusSecretName,
            &lusSecretData);
        dwRetCode = LsaNtStatusToWinError(ntsResult);
    }

    LsaClose(LsaPolicyHandle);

    if (dwRetCode != ERROR_SUCCESS)
        wprintf(L"Failed call to LsaStorePrivateData %lu\n",
            dwRetCode);
    
    return dwRetCode;

}

```



<span data-ttu-id="28b37-111">Tenga en cuenta que si Winlogon no puede encontrar una contraseña almacenada por la función [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) , usará el valor **DefaultPassword** de la clave Winlogon (si existe) para la contraseña de inicio de sesión automático.</span><span class="sxs-lookup"><span data-stu-id="28b37-111">Note that if Winlogon cannot find a password stored by the [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) function, it will use the **DefaultPassword** value of the Winlogon key (if it exists) for the automatic logon password.</span></span>

<span data-ttu-id="28b37-112">Para obtener más información sobre el inicio de sesión automático y la clave del registro Winlogon, vea [ características deMSGina.dll](msgina-dll-features.md).</span><span class="sxs-lookup"><span data-stu-id="28b37-112">For more information about automatic logon and the Winlogon registry key, see [MSGina.dll Features](msgina-dll-features.md).</span></span>

<span data-ttu-id="28b37-113">Para obtener más información sobre cómo proteger las contraseñas, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="28b37-113">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

 

 
