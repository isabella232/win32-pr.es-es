---
title: Obtención del nombre de Account-Style de dominio de un grupo
description: Los usuarios, grupos, equipos y otras entidades de seguridad se pueden representar en el formulario de cuenta de dominio.
ms.assetid: 85627d2d-2845-4998-9957-ce0c8b6473bd
ms.tgt_platform: multiple
keywords:
- agrupa AD, obteniendo el nombre del estilo de la cuenta de dominio de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758e61072b862f7c4cd1581b8d54dafb38915be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903119"
---
# <a name="getting-the-domain-account-style-name-of-a-group"></a><span data-ttu-id="accac-104">Obtención del nombre de Account-Style de dominio de un grupo</span><span class="sxs-lookup"><span data-stu-id="accac-104">Getting the Domain Account-Style Name of a Group</span></span>

<span data-ttu-id="accac-105">Los usuarios, grupos, equipos y otras entidades de seguridad se pueden representar en el formulario de cuenta de dominio.</span><span class="sxs-lookup"><span data-stu-id="accac-105">Users, groups, computers, and other security principals can be represented in domain account form.</span></span> <span data-ttu-id="accac-106">Cuenta de dominio (el nombre de inicio de sesión usado en versiones anteriores de Windows NT) tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="accac-106">Domain account (the logon name used in earlier versions of Windows NT) has the following form:</span></span>


```C++
<domain>\<account>
```



<span data-ttu-id="accac-107">Donde " <domain> " es el nombre del dominio de Windows NT que contiene el usuario y " <account> " es la propiedad **samAccountName** del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="accac-107">Where "<domain>" is the name of the Windows NT domain that contains the user and "<account>" is the **samAccountName** property of the specified user.</span></span> <span data-ttu-id="accac-108">Por ejemplo: "fabrikam \\ juanpérez".</span><span class="sxs-lookup"><span data-stu-id="accac-108">For example: "Fabrikam\\jeffsmith".</span></span>

<span data-ttu-id="accac-109">El formulario de cuenta de dominio puede especificar el administrador de confianza en una ACE en un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="accac-109">The domain account form can specify the trustee in an ACE in a security descriptor.</span></span> <span data-ttu-id="accac-110">También se utiliza para el nombre de inicio de sesión en equipos que ejecutan Windows versión NT 4,0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="accac-110">It is also used for the logon name on computers running Windows version NT 4.0 and earlier.</span></span>


```C++
// Need to include the following headers to use DsGetDcName.
// #include <LMCONS.H>
// #include <Dsgetdc.h>
// #include <Lmapibuf.h>
// This function returns the previous version name of the security principal 
// specified by the distinguished name specified by szDN.
// The szDomain parameter should be NULL to use the current domain
// to get the name translation. Otherwise, specify the domain to use as the
// domain name (such as liliput) 
// or in dotted format (such as lilliput.Fabrikam.com).
HRESULT GetDownlevelName(LPOLESTR szDomainName, LPOLESTR szDN, LPOLESTR *ppNameString)
{
HRESULT hr = E_FAIL;
IADsNameTranslate *pNameTr = NULL;
IADs *pObject = NULL;
CComBSTR sbstrInitDomain = "";
 
if ((!szDN)||(!ppNameString))
{
    return hr;
}
 
// Use the current domain if none is specified.
if (!szDomainName)
{
    // Call DsGetDcName to get the name of this computer's domain.
    PDOMAIN_CONTROLLER_INFO DomainControllerInfo = NULL;
    DWORD dReturn = 0L;
    dReturn = DsGetDcName(  NULL,
                NULL,
                NULL,
                NULL,
                DS_DIRECTORY_SERVICE_REQUIRED,
                &DomainControllerInfo
    );
    if (dReturn==NO_ERROR)
    {
        sbstrInitDomain = DomainControllerInfo->DomainName;
        hr = S_OK;
    }
 
    // Free the buffer.
    if (DomainControllerInfo)
        NetApiBufferFree(DomainControllerInfo);
}
else
{
    sbstrInitDomain = szDomainName;
    hr = S_OK;
}
 

if (SUCCEEDED(hr))
{
 
    // Create the COM object for the IADsNameTranslate object.
    hr  = CoCreateInstance( 
                                CLSID_NameTranslate,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IADsNameTranslate,
                                (void **)&pNameTr
                          );
    if (SUCCEEDED(hr))
    {
 
        // Initialize for the specified domain.
        hr = pNameTr->Init(ADS_NAME_INITTYPE_DOMAIN, sbstrInitDomain);
        if (SUCCEEDED(hr))
        {
            CComBSTR sbstrNameTr;

            hr = pNameTr->Set(ADS_NAME_TYPE_1779, CComBSTR(szDN));
            hr = pNameTr->Get(ADS_NAME_TYPE_NT4, &sbstrNameTr);
            if (SUCCEEDED(hr))
            {
                *ppNameString = (OLECHAR *)CoTaskMemAlloc (sizeof(OLECHAR)*(sbstrNameTr.Length() + 1));
                if (*ppNameString)
                    wcscpy_s(*ppNameString, sbstrNameTr);
                else
                    hr=E_FAIL;
            }
        }

        pNameTr->Release();
    }
}
 
// Caller must call CoTaskMemFree to free ppNameString.
return hr;
}
```



 

 




