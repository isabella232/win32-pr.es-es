---
title: IADsDeleteOps (interfaz)
description: La interfaz IADsDeleteOps se usa en rutinas de supervisión y mantenimiento para el almacén de directorios subyacente. Puede eliminar objetos hoja y subárboles completos en una sola operación.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- ADSI de interfaz IADsDeleteOps
- IADsDeleteOps ADSI , mediante
- ADSI ADSI , código de ejemplo C/C++, con IADsDeleteOps para eliminar grupos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839948"
---
# <a name="iadsdeleteops-interface"></a>IADsDeleteOps (interfaz)

La [**interfaz IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) se usa en rutinas de supervisión y mantenimiento para el almacén de directorios subyacente. Puede eliminar objetos hoja y subárboles completos en una sola operación.

Si no se admite esta interfaz, la eliminación de un objeto de Active Directory requeriría que cada objeto contenido se enumerase y eliminara de forma recursiva. Con esta interfaz, cualquier objeto contenedor, con todos sus objetos y subobjetos contenidos, se puede eliminar con una sola operación.

En el ejemplo de código siguiente se elimina el contenedor "Eng" y todos los objetos secundarios.


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



En el ejemplo de código siguiente se elimina el contenedor "Eng" y todos los objetos secundarios.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




