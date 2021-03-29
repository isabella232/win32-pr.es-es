---
title: Habilitar los cambios de esquema en el maestro de esquema
description: De forma predeterminada, la modificación del esquema está deshabilitada en todos los controladores de dominio de Windows 2000.
ms.assetid: 08806a9e-283c-48d9-9557-bcb9719fc13c
ms.tgt_platform: multiple
keywords:
- Habilitación de los cambios de esquema en el AD maestro de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840c9928011179ce303c83f4d00ef598f38eb64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993907"
---
# <a name="enabling-schema-changes-at-the-schema-master"></a><span data-ttu-id="b36f6-104">Habilitar los cambios de esquema en el maestro de esquema</span><span class="sxs-lookup"><span data-stu-id="b36f6-104">Enabling Schema Changes at the Schema Master</span></span>

<span data-ttu-id="b36f6-105">De forma predeterminada, la modificación del esquema está deshabilitada en todos los controladores de dominio de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b36f6-105">By default, schema modification is disabled on all Windows 2000 domain controllers.</span></span> <span data-ttu-id="b36f6-106">La capacidad de actualizar el esquema se controla mediante el siguiente valor del registro en el controlador de dominio del maestro del esquema:</span><span class="sxs-lookup"><span data-stu-id="b36f6-106">The ability to update the schema is controlled by the following registry value on the schema master domain controller:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            NTDS
               Parameters
                  Schema Update Allowed
```

<span data-ttu-id="b36f6-107">Este valor del registro es un valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b36f6-107">This registry value is a **REG\_DWORD** value.</span></span> <span data-ttu-id="b36f6-108">Si este valor no está presente o contiene cero (0), se deshabilita la modificación del esquema.</span><span class="sxs-lookup"><span data-stu-id="b36f6-108">If this value is not present or contains zero (0), then schema modification is disabled.</span></span> <span data-ttu-id="b36f6-109">Si este valor está presente y contiene un valor distinto de cero, la modificación del esquema está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b36f6-109">If this value is present and contains a value other than zero, then schema modification is enabled.</span></span>

<span data-ttu-id="b36f6-110">El complemento MMC del administrador de esquemas proporciona al usuario la posibilidad de habilitar o deshabilitar manualmente la modificación del esquema.</span><span class="sxs-lookup"><span data-stu-id="b36f6-110">The Schema Manager MMC snap-in provides the user with the ability to manually enable or disable schema modification.</span></span> <span data-ttu-id="b36f6-111">La modificación del esquema se puede habilitar o deshabilitar mediante programación modificando este valor del registro en el controlador de dominio del maestro del esquema.</span><span class="sxs-lookup"><span data-stu-id="b36f6-111">Schema modification can be enabled or disabled programmatically by modifying this registry value on the schema master domain controller.</span></span>

<span data-ttu-id="b36f6-112">La siguiente función de C++ muestra cómo determinar si el esquema se puede modificar en un maestro de esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="b36f6-112">The following C++ function shows how to determine if the schema can be modified on a specified schema master.</span></span>


```C++
HRESULT IsSchemaUpdateEnabled(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL *pfEnabled)
{
    *pfEnabled = FALSE;
  
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    tcscpy_s(pszPath, szPrefix);
    tcscat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szKeyPath, 
            0, 
            KEY_READ, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwType;
            DWORD dwValue;
            DWORD dwSize;

            dwSize = sizeof(dwValue);
            lReturn = RegQueryValueEx(
                hKeyParameters, 
                szValueName, 
                0, 
                &dwType, 
                (LPBYTE)&dwValue, 
                &dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                *pfEnabled = (0 != dwValue);
                
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
  
    return hr;
}
```



<span data-ttu-id="b36f6-113">La siguiente función de C++ muestra cómo habilitar o deshabilitar la modificación de esquemas en un maestro de esquema especificado.</span><span class="sxs-lookup"><span data-stu-id="b36f6-113">The following C++ function shows how to enable or disable schema modification on a specified schema master.</span></span>


```C++
HRESULT EnableSchemaUpdate(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL fEnabled)
{
    
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    strcpy_s(pszPath, szPrefix);
    strcat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szRelKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szRelKeyPath, 
            0, 
            KEY_SET_VALUE, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwValue;
            DWORD dwSize;

            if(fEnabled)
            {
                dwValue = 1;
            }
            else
            {
                dwValue = 0;
            }
            
            dwSize = sizeof(dwValue);
            lReturn = RegSetValueEx(
                hKeyParameters, 
                szValueName, 
                0L, 
                REG_DWORD, 
                (LPBYTE)&dwValue, 
                dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
    
    return hr;
}
```



 

 




