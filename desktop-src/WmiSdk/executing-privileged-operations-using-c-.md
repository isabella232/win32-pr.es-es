---
description: Las aplicaciones cliente especiales pueden invocar operaciones con privilegios.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Ejecución de operaciones con privilegios mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e83667cd4a4cd81439392f1f58d77fb56109f79c2dd6d826c9390d62008553b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050893"
---
# <a name="executing-privileged-operations-using-c"></a>Ejecución de operaciones con privilegios mediante C++

Las aplicaciones cliente especiales pueden invocar operaciones con privilegios. Por ejemplo, una aplicación podría permitir que un administrador reinicie un equipo de oficina que no responde. Mediante el Windows Management Instrumentation (WMI), puede ejecutar una operación con privilegios llamando al proveedor WMI para la operación con privilegios.

En el procedimiento siguiente se describe cómo llamar a un proveedor para una operación con privilegios.

**Para llamar a un proveedor para una operación con privilegios**

1.  Obtenga permisos para que el proceso de cliente ejecute la operación con privilegios.

    Normalmente, un administrador establece los permisos mediante herramientas administrativas del sistema, antes de ejecutar el proceso.

2.  Obtenga el permiso para el proceso de proveedor para habilitar la operación con privilegios.

    Normalmente, puede establecer permisos de proveedor con una llamada a la [**función AdjustTokenPrivileges.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)

3.  Obtenga el permiso para el proceso de cliente para habilitar la operación con privilegios.

    Este paso solo es necesario si el proveedor es local para el cliente. Si el cliente y el proveedor existen en el mismo equipo, el cliente debe habilitar específicamente la operación con privilegios mediante una de las técnicas siguientes:

    -   Si el cliente posee el proceso, el cliente puede usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para ajustar el token de proceso antes de llamar a WMI. En este caso, no es necesario codificar más.
    -   Si el cliente no puede acceder al token de cliente, el cliente puede usar el siguiente procedimiento para crear un token de subproceso y usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en ese token.

En el procedimiento siguiente se describe cómo crear un token de subproceso y usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en ese token.

**Para crear un token de subproceso y usar AdjustTokenPrivileges en ese token**

1.  Cree una copia del token de proceso mediante una [**llamada a ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).
2.  Recupere el token de subproceso recién creado mediante una [**llamada a GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).
3.  Habilite la operación con privilegios con una llamada a [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en el nuevo token.
4.  Obtenga un puntero a [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
5.  Oculte el puntero a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
6.  Repita los pasos del 1 al 5 en cada llamada a WMI.

    > [!Note]  
    > Debe repetir los pasos porque COM almacena en caché los tokens incorrectamente.

     

El ejemplo de código de este tema requiere que la siguiente \# instrucción include se compile correctamente.


```C++
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo habilitar privilegios en un equipo local.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
