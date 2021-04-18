---
description: Una comprobación de acceso determina si un descriptor de seguridad concede un conjunto especificado de derechos de acceso al cliente o subproceso identificado por un token de acceso.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Realización de comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706754"
---
# <a name="performing-access-checks"></a><span data-ttu-id="6e5c4-103">Realización de comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="6e5c4-103">Performing Access Checks</span></span>

<span data-ttu-id="6e5c4-104">Una comprobación de acceso determina si un descriptor de seguridad concede un conjunto especificado de derechos de acceso al cliente o subproceso identificado por un token de acceso.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="6e5c4-105">Puede llamar a la función de seguridad [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) desde aplicaciones cliente WMI o proveedores escritos en C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="6e5c4-106">Los scripts y las aplicaciones Visual Basic no pueden realizar comprobaciones de acceso mediante el método que se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="6e5c4-107">Las aplicaciones cliente deben realizar una comprobación de acceso para determinar la identidad de la devolución de llamada al devolver los resultados al receptor proporcionado por la llamada asincrónica del cliente.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="6e5c4-108">Cuando los proveedores no pueden suplantar la aplicación cliente o el script que solicita datos, deben realizar comprobaciones de acceso en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="6e5c4-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="6e5c4-109">Al tener acceso a recursos que no están protegidos por listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="6e5c4-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="6e5c4-110">Cuando el cliente se ha conectado en el nivel de suplantación de **RPC \_ C, \_ \_ identifique** .</span><span class="sxs-lookup"><span data-stu-id="6e5c4-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="6e5c4-111">Las aplicaciones de C++ y C# pueden controlar si las comprobaciones de acceso se realizan en un proceso independiente.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="6e5c4-112">Los scripts y las aplicaciones Visual Basic pueden leer o cambiar una clave del registro para asegurarse de que WMI realiza comprobaciones de acceso.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="6e5c4-113">Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="6e5c4-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="6e5c4-114">El ejemplo de código de este tema requiere las siguientes referencias e \# incluir instrucciones para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


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



<span data-ttu-id="6e5c4-115">En el ejemplo de código siguiente se muestra cómo comprobar que el token de seguridad de un subproceso de la aplicación cliente contiene permisos adecuados para un descriptor de seguridad especificado.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="6e5c4-116">La función toma la cadena "domain \\ User" y devuelve el SID.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="6e5c4-117">Si se produce un error en la llamada, la función devuelve **null**; de lo contrario, el llamador debe liberar el puntero devuelto.</span><span class="sxs-lookup"><span data-stu-id="6e5c4-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6e5c4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e5c4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e5c4-119">Elección del registro correcto</span><span class="sxs-lookup"><span data-stu-id="6e5c4-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="6e5c4-120">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="6e5c4-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="6e5c4-121">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="6e5c4-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="6e5c4-122">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="6e5c4-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
