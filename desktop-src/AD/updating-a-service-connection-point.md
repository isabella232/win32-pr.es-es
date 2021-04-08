---
title: Actualización de un punto de conexión de servicio
description: En el ejemplo de código siguiente se muestra cómo actualizar un punto de conexión de servicio. Normalmente, un servicio ejecuta este código cuando se inicia.
ms.assetid: 315fb2b5-d071-4420-95fb-ab680296b3cf
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77558f9ac10b2c2a908266f1b4e021862af0c629
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904467"
---
# <a name="updating-a-service-connection-point"></a><span data-ttu-id="03981-104">Actualización de un punto de conexión de servicio</span><span class="sxs-lookup"><span data-stu-id="03981-104">Updating a Service Connection Point</span></span>

<span data-ttu-id="03981-105">En el ejemplo de código siguiente se muestra cómo actualizar un punto de conexión de servicio.</span><span class="sxs-lookup"><span data-stu-id="03981-105">The following code example shows how to update a service connection point.</span></span> <span data-ttu-id="03981-106">Normalmente, un servicio ejecuta este código cuando se inicia.</span><span class="sxs-lookup"><span data-stu-id="03981-106">This code is typically executed by a service when it starts.</span></span>

<span data-ttu-id="03981-107">En este ejemplo se recupera la cadena de enlace del GUID del SCP que el instalador del servicio almacenó en caché en el registro.</span><span class="sxs-lookup"><span data-stu-id="03981-107">This example retrieves the SCP's GUID binding string that the service installer cached in the registry.</span></span> <span data-ttu-id="03981-108">Usa esta cadena para enlazar con un puntero [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) en el objeto SCP y, a continuación, llama al método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para obtener los atributos **serviceDNSName** y **serviceBindingInformation** del SCP.</span><span class="sxs-lookup"><span data-stu-id="03981-108">It uses this string to bind to an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) pointer on the SCP object, and then calls the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the **serviceDNSName** and **serviceBindingInformation** attributes of the SCP.</span></span> <span data-ttu-id="03981-109">Tenga en cuenta que es posible que el servicio requiera comprobar y actualizar atributos adicionales.</span><span class="sxs-lookup"><span data-stu-id="03981-109">Be aware that your service may require to verify and update additional attributes.</span></span>

<span data-ttu-id="03981-110">El código compara el valor de **serviceDNSName** con el nombre DNS devuelto por la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="03981-110">The code compares the **serviceDNSName** value to the DNS name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span> <span data-ttu-id="03981-111">También compara el número de puerto actual del servicio con el número de Puerto almacenado en el atributo **serviceBindingInformation** .</span><span class="sxs-lookup"><span data-stu-id="03981-111">It also compares the service's current port number to the port number stored in the **serviceBindingInformation** attribute.</span></span> <span data-ttu-id="03981-112">Si alguno de estos valores ha cambiado, el código llama al método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) para actualizar los atributos de SCP.</span><span class="sxs-lookup"><span data-stu-id="03981-112">If either of these values have changed, the code calls the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) method to update the SCP attributes.</span></span>


```C++
DWORD
ScpUpdate(USHORT usPort)
{
DWORD   dwStat, dwType, dwLen;
BOOL    bUpdate=FALSE;

HKEY    hReg;

TCHAR   szAdsPath[MAX_PATH];
TCHAR   szServer[MAX_PATH];
TCHAR   szPort[8];
TCHAR   *pszAttrs[]={
    {TEXT("serviceDNSName")},
    {TEXT("serviceBindingInformation")},
};

HRESULT             hr;
IDirectoryObject    *pObj;
DWORD               dwAttrs;
int                 i;

PADS_ATTR_INFO  pAttribs;
ADSVALUE        dnsname,binding;

ADS_ATTR_INFO   Attribs[]={
    {TEXT("serviceDnsName"),ADS_ATTR_UPDATE,ADSTYPE_CASE_IGNORE_STRING,&dnsname,1},
    {TEXT("serviceBindingInformation"),ADS_ATTR_UPDATE,ADSTYPE_CASE_IGNORE_STRING,&binding,1},
};

// Open the service registry key.
dwStat = RegOpenKeyEx(
        HKEY_LOCAL_MACHINE,
        TEXT("Software\\Microsoft\\Windows 2000 Auth-O-Matic"),
        0,
        KEY_QUERY_VALUE,
        &hReg);
if (dwStat != NO_ERROR) 
{
    ReportServiceError("RegOpenKeyEx failed", dwStat);
    return dwStat;
}

// Get the GUID binding string used to bind to the service SCP.
dwLen = sizeof(szAdsPath);
dwStat = RegQueryValueEx(hReg, TEXT("GUIDBindingString"), 0, &dwType, 
                             (LPBYTE)szAdsPath, &dwLen);
if (dwStat != NO_ERROR) {
    ReportServiceError("RegQueryValueEx failed", dwStat);
    return dwStat;
}

RegCloseKey(hReg);

// Bind to the SCP.
hr = ADsGetObject(szAdsPath, IID_IDirectoryObject, (void **)&pObj);
if (FAILED(hr)) 
{
    char szMsg1[1024];
    sprintf_s(szMsg1, 
            "ADsGetObject failed to bind to GUID (bind string: %S): ", 
            szAdsPath);
    ReportServiceError(szMsg1, hr);
    if(pObj)
    {
        pObj->Release();
    }
    return dwStat;
}

// Retrieve attributes from the SCP.
hr = pObj->GetObjectAttributes(pszAttrs, 2, &pAttribs, &dwAttrs);
if (FAILED(hr)) {
    ReportServiceError("GetObjectAttributes failed", hr);
    pObj->Release();
    return hr;
}

// Get the current port and DNS name of the host server.
_stprintf_s(szPort,TEXT("%d"),usPort);
dwLen = sizeof(szServer);
if (!GetComputerNameEx(ComputerNameDnsFullyQualified,szServer,&dwLen)) 
{
    pObj->Release();
    return GetLastError();
}

// Compare the current DNS name and port to the values retrieved from
// the SCP. Update the SCP only if nothing has changed.
for (i=0; i<(LONG)dwAttrs; i++) 
{
    if ((_tcscmp(TEXT("serviceDNSName"),pAttribs[i].pszAttrName)==0) &&
        (pAttribs[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING))
    {
        if (_tcscmp(szServer,pAttribs[i].pADsValues->CaseIgnoreString) != 0)
        {
            ReportServiceError("serviceDNSName being updated", 0);
            bUpdate = TRUE;
        }
        else
            ReportServiceError("serviceDNSName okay", 0);

    }

    if ((_tcscmp(TEXT("serviceBindingInformation"),pAttribs[i].pszAttrName)==0) &&
        (pAttribs[i].dwADsType == ADSTYPE_CASE_IGNORE_STRING))
    {
        if (_tcscmp(szPort,pAttribs[i].pADsValues->CaseIgnoreString) != 0)
        {
            ReportServiceError("serviceBindingInformation being updated", 0);
            bUpdate = TRUE;
        }
        else
            ReportServiceError("serviceBindingInformation okay", 0);
    }
}

FreeADsMem(pAttribs);

// The binding data or server name have changed, 
// so update the SCP values.
if (bUpdate)
{
    dnsname.dwType              = ADSTYPE_CASE_IGNORE_STRING;
    dnsname.CaseIgnoreString    = szServer;
    binding.dwType              = ADSTYPE_CASE_IGNORE_STRING;
    binding.CaseIgnoreString    = szPort;
    hr = pObj->SetObjectAttributes(Attribs, 2, &dwAttrs);
    if (FAILED(hr)) 
    {
        ReportServiceError("ScpUpdate: Failed to set SCP values.", hr);
        pObj->Release();
        return hr;
    }
}

pObj->Release();

return dwStat;
}
```



 

 