---
title: Interfaz IADsDeleteOps
description: La interfaz IADsDeleteOps se usa en las rutinas de supervisión y mantenimiento para el almacén de directorios subyacente. Puede eliminar objetos hoja y subárboles completos en una sola operación.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Interfaz IADsDeleteOps ADSI
- IADsDeleteOps ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsDeleteOps para eliminar grupos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656175"
---
# <a name="iadsdeleteops-interface"></a>Interfaz IADsDeleteOps

La interfaz [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) se usa en las rutinas de supervisión y mantenimiento para el almacén de directorios subyacente. Puede eliminar objetos hoja y subárboles completos en una sola operación.

Si no se admite esta interfaz, la eliminación de un objeto de Active Directory requeriría que cada objeto contenido se Enumere y se eliminara de forma recursiva. Con esta interfaz, cualquier objeto contenedor, con todos sus objetos y subobjetos contenidos, se puede eliminar con una sola operación.

En el ejemplo de código siguiente se elimina el contenedor "ENG" y todos los objetos secundarios.


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



En el ejemplo de código siguiente se elimina el contenedor "ENG" y todos los objetos secundarios.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




