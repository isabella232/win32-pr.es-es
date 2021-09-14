---
title: Extensión de clase auxiliar NDF
description: En este ejemplo se muestra cómo implementar funciones de diagnóstico y reparación de NDF.
ms.assetid: 18e66d09-e565-4b86-8bc3-600f2159a4bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b2a0dbcba29449b8f21850fa0669f8154dcbd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161195"
---
# <a name="ndf-helper-class-extension"></a>Extensión de clase auxiliar NDF

En este ejemplo se muestra cómo implementar funciones de diagnóstico y reparación de NDF. En este ejemplo, debe existir un archivo de configuración crítico para que el sistema siga siendo correcto. En consecuencia, el problema es determinar si el archivo existe. Si no es así, el sistema es incorrecto y NDF diagnostica el problema. La reparación es volver a crear el archivo que falta.

Para diagnosticar y reparar el problema es necesario usar cuatro métodos [**INetDiagHelper:**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize), [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo)y [**Repair**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair).

## <a name="initializing-the-helper-class"></a>Inicialización de la clase auxiliar

Inicialice y recupere el nombre del archivo que se buscará. Este nombre de archivo se pasa durante el diagnóstico como un atributo auxiliar denominado "filename".


```C++
#include <windows.h>
//utility function to simplify string allocation and copies, user throughout example
HRESULT 
StringCchCopyWithAlloc (
    PWSTR* Dest, 
    size_t cchMaxLen,
    in PCWSTR Src)
{
    if (NULL == Dest || NULL == Src || cchMaxLen > USHRT_MAX)
    {
        return E_INVALIDARG;
    }
    size_t cchSize = 0;

    HRESULT hr = StringCchLength(Src, cchMaxLen - 1, &cchSize); 
    if (FAILED(hr))
    {
        return hr;
    }

    size_t cbSize = (cchSize + 1)*sizeof(WCHAR);
    *Dest = (PWSTR) CoTaskMemAlloc(cbSize);
    if (NULL == *Dest)
    {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(*Dest, cbSize);

    return StringCchCopy((STRSAFE_LPWSTR)*Dest, cchSize + 1, Src);    
}

HRESULT SimpleFileHelperClass::Initialize(
        /* [in] */ ULONG celt,
        /* [size_is][in] */ HELPER_ATTRIBUTE rgAttributes[  ])
{
    if(celt < 1)
    {
        return E_INVALIDARG;
    }
    if(rgAttributes == NULL)
    {
        return E_INVALIDARG; 
    }
    else
    {
        //verify the attribute is named as expected
        if (wcscmp(rgAttributes[0].pwszName, L"filename")==0)
        {
            //copy the attribute to member variable
            return StringCchCopyWithAlloc(&m_pwszTestFile, MAX_PATH, 
                    rgAttributes[0].PWStr);
        } else {
            //the attribute isn't named as expected
            return E_INVALIDARG;
        }
    }
}

```



## <a name="checking-on-the-files-existence"></a>Comprobación de la existencia del archivo

El [**método LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) se usa para comprobar la existencia del archivo. Si el archivo existe, el estado de diagnóstico se establece en **DS \_ REJECTED**, lo que indica que no hay nada incorrecto. Si no se encuentra el archivo, el estado de diagnóstico se establece en **DS \_ CONFIRMED**.


```C++
#include <windows.h>

HRESULT SimpleFileHelperClass::LowHealth( 
            /* [unique][string][in] */ LPCWSTR pwszInstanceDescription,
            /* [string][out] */ LPWSTR *ppwszDescription,
            /* [out] */ long *pDeferredTime,
            /* [out] */ DIAGNOSIS_STATUS *pStatus) 

{
    HANDLE hFile = NULL;
    LPWSTR pwszDiagString=NULL;
    // does the file already exist?
    hFile = CreateFile(
        m_pwszTestFile, 
        GENERIC_READ, 
        0, 
        NULL, 
        OPEN_EXISTING, 
        FILE_ATTRIBUTE_NORMAL, 
        NULL);

    if(INVALID_HANDLE_VALUE == hFile)
    { 
        // alloc and set the diagnosis description and status
        HRESULT hr = StringCchCopyWithAlloc(&pwszDiagString, MAX_PATH, 
                    L"The file was deleted.");
        if (FAILED(hr))
        {
            return hr;
        }
  
        *ppwszDescription = pwszDiagString;
        *pStatus = DS_CONFIRMED;
        return S_OK;
    }
    CloseHandle(hFile); 
    
    //the file exists
    *pStatus = DS_REJECTED;
    return S_OK;
}
```



## <a name="determining-the-repair-action"></a>Determinar la acción de reparación

Si [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) devuelve **DS \_ CONFIRMED**, [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo) se implementa para determinar la acción de reparación adecuada. En este ejemplo, eso significa volver a crear el archivo.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::GetRepairInfo( 
            /* [in] */ PROBLEM_TYPE problem,
            /* [out] */ ULONG *pcelt,
            /* [size_is][size_is][out] */ RepairInfo **ppInfo)
{
    HRESULT hr=S_OK;
    RepairInfo* pRepair = (RepairInfo *)CoTaskMemAlloc(sizeof(RepairInfo));
    if (pRepair == NULL) {
        return E_OUTOFMEMORY;
    }
    SecureZeroMemory(pRepair,sizeof(RepairInfo));

    // set the repair description and class name
    hr = StringCchCopyWithAlloc(&pRepair->pwszClassName, MAX_PATH,
                L"SimpleFileHelperClass");
    if (FAILED(hr))
    {
        goto Error;
    }

    hr = StringCchCopyWithAlloc(&pRepair->pwszDescription, MAX_PATH, 
                L"Low Health Repair");
    if (FAILED(hr))
    {
        goto Error;
    }
  
    // set the resolution GUID and cost
    pRepair->guid = ID_LowHealthRepair;
    pRepair->cost = 0;
    // set repair status flags
    pRepair->sidType = WinWorldSid;
    pRepair->scope = RS_SYSTEM;
    pRepair->risk = RR_NORISK;
    pRepair->flags |= DF_IMPERSONATION; //impersonate the user when repairing
    pRepair->UiInfo.type = UIT_NONE;
    
    //pass back the repair
    *ppInfo = pRepair; 
    *pcelt = 1; //number of repairs

    return S_OK;

Error:
    if(pRepair){
        if(pRepair->pwszClassName){
            CoTaskMemFree(pRepair->pwszClassName);
        }
        if(pRepair->pwszDescription){
            CoTaskMemFree(pRepair->pwszDescription);
        }
    }
    return hr;
}

```



## <a name="repairing-the-problem"></a>Reparación del problema

Al usuario se le presentan las opciones de corrección devueltas por [**GetRepairInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getrepairinfo), a menos que solo haya una opción de reparación, en cuyo caso se ejecuta automáticamente. Se [**llama al**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-repair) método Repair con la estructura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) aplicable para que se pueda restaurar el archivo de configuración.


```C++
#include <windows.h>

HRESULT  
SimpleFileHelperClass::Repair( 
            /* [in] */ RepairInfo *pInfo,
            /* [out] */ long *pDeferredTime,
            /* [out] */ REPAIR_STATUS *pStatus)
{
    //verify expected repair was requested
    if(IsEqualGUID(ID_LowHealthRepair, pInfo->guid)){
        HANDLE hFile = NULL;
        hFile = CreateFile(m_pwszTestFile, 
                                GENERIC_WRITE, 
                                0, 
                                NULL, 
                                CREATE_ALWAYS,
                                FILE_ATTRIBUTE_NORMAL, 
                                NULL);
        if(INVALID_HANDLE_VALUE == hFile)
        {
            // repair failed
            *pStatus = RS_UNREPAIRED;
            return HRESULT_FROM_WIN32(GetLastError());
        }
        CloseHandle(hFile);
        
        // repair succeeded
        *pStatus = RS_REPAIRED;
    } else {
        return E_INVALIDARG; //unkown repair passed in
    }
    return S_OK;
}
```



 

 




