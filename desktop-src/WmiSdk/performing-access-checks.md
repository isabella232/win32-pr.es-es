---
description: Una comprobación de acceso determina si un descriptor de seguridad concede un conjunto especificado de derechos de acceso al cliente o subproceso identificado por un token de acceso.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Realizar comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e06f2bccab886b38b53ecc3592371555b8c93a0ed12cdad0a4f039b62d62752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050513"
---
# <a name="performing-access-checks"></a>Realizar comprobaciones de acceso

Una comprobación de acceso determina si un descriptor de seguridad concede un conjunto especificado de derechos de acceso al cliente o subproceso identificado por un token de acceso. Puede llamar a la función de seguridad [**AccessCheck desde**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) aplicaciones cliente WMI o proveedores escritos en C++ o C#. Los scripts Visual Basic aplicaciones no pueden realizar comprobaciones de acceso mediante el método descrito aquí.

Las aplicaciones cliente deben realizar una comprobación de acceso para determinar la identidad de la devolución de llamada al devolver los resultados al receptor proporcionado por la llamada asincrónica del cliente.

Cuando los proveedores no pueden suplantar la aplicación cliente o el script que solicita datos, deben realizar comprobaciones de acceso para las situaciones siguientes:

-   Al acceder a recursos que no están protegidos por listas de control de acceso (ACL).
-   Cuando el cliente se ha conectado en el nivel **de suplantación RPC C LEVEL \_ \_ \_ IDENTIFY.**

> [!Note]  
> Las aplicaciones de C++ y C# pueden controlar si las comprobaciones de acceso se realizan mediante un proceso independiente. Los scripts Visual Basic aplicaciones pueden leer o cambiar una clave del Registro para asegurarse de que WMI realiza comprobaciones de acceso. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

 

El ejemplo de código de este tema requiere las siguientes referencias e \# instrucciones include para compilarse correctamente.


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



En el ejemplo de código siguiente se muestra cómo comprobar que el token de seguridad de un subproceso de aplicación cliente contiene los permisos adecuados para un descriptor de seguridad especificado. La función toma la cadena "usuario \\ de dominio" y devuelve el SID. Si se produce un error en la llamada, la función **devuelve NULL;** de lo contrario, el autor de la llamada debe liberar el puntero devuelto.


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elección del registro correcto](choosing-correct-registration.md)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
