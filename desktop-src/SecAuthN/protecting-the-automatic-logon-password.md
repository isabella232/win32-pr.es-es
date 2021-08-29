---
description: La contraseña de inicio de sesión automático debe protegerse mediante la función LsaStorePrivateData.
ms.assetid: 7bd4d725-de17-4801-bd06-8d47a777409d
title: Protección de la contraseña de inicio de sesión automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43435afaef5820bdfeb8eda1c092904858e05f11de2f718450f5b5c76058bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920673"
---
# <a name="protecting-the-automatic-logon-password"></a>Protección de la contraseña de inicio de sesión automático

La contraseña de inicio de sesión automático debe protegerse mediante la [**función LsaStorePrivateData.**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata)

En el ejemplo siguiente se muestra cómo proteger la contraseña de inicio de sesión automático. En el ejemplo se recupera un identificador para el [**objeto Policy**](../secmgmt/policy-object.md) mediante una llamada a la [**función LsaOpenPolicy.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopenpolicy) Para obtener más información  sobre los **identificadores de** objeto de directiva y de objeto de directiva, vea Objeto **de** directiva y Apertura de un identificador de objeto [de](../secmgmt/opening-a-policy-object-handle.md)directiva , respectivamente. A continuación, el ejemplo establece la contraseña protegida mediante una llamada a [**la función LsaStorePrivateData.**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) Tenga en cuenta que si el autor de la llamada pasa **NULL para** el valor de contraseña protegida, el código borra la contraseña protegida existente. Antes de salir, el código cierra el identificador al **objeto Policy.**


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



Tenga en cuenta que si Winlogon no encuentra una contraseña almacenada por la función [**LsaStorePrivateData,**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) usará el valor **DefaultPassword** de la clave Winlogon (si existe) para la contraseña de inicio de sesión automático.

Para obtener más información sobre el inicio de sesión automático y la clave del Registro Winlogon, [ veaMSGina.dll características](msgina-dll-features.md).

Para obtener más información sobre la protección de contraseñas, vea [Control de contraseñas.](../secbp/handling-passwords.md)

 

 
