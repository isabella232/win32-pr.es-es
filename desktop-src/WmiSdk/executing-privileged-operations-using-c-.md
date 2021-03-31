---
description: Las aplicaciones cliente especiales podrían invocar operaciones con privilegios.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Ejecutar operaciones con privilegios mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360582"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="87d99-103">Ejecutar operaciones con privilegios mediante C++</span><span class="sxs-lookup"><span data-stu-id="87d99-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="87d99-104">Las aplicaciones cliente especiales podrían invocar operaciones con privilegios.</span><span class="sxs-lookup"><span data-stu-id="87d99-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="87d99-105">Por ejemplo, una aplicación podría permitir que un administrador reinicie un equipo de Office que no responde.</span><span class="sxs-lookup"><span data-stu-id="87d99-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="87d99-106">Mediante el uso de Instrumental de administración de Windows (WMI), puede ejecutar una operación con privilegios llamando al proveedor WMI para la operación con privilegios.</span><span class="sxs-lookup"><span data-stu-id="87d99-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="87d99-107">En el procedimiento siguiente se describe cómo llamar a un proveedor para una operación con privilegios.</span><span class="sxs-lookup"><span data-stu-id="87d99-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="87d99-108">**Para llamar a un proveedor para una operación con privilegios**</span><span class="sxs-lookup"><span data-stu-id="87d99-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="87d99-109">Obtener permisos para que el proceso de cliente ejecute la operación privilegiada.</span><span class="sxs-lookup"><span data-stu-id="87d99-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="87d99-110">Normalmente, un administrador establece los permisos mediante herramientas administrativas del sistema, antes de ejecutar el proceso.</span><span class="sxs-lookup"><span data-stu-id="87d99-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="87d99-111">Obtiene el permiso para que el proceso del proveedor habilite la operación privilegiada.</span><span class="sxs-lookup"><span data-stu-id="87d99-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="87d99-112">Normalmente, puede establecer permisos de proveedor con una llamada a la función [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="87d99-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="87d99-113">Obtiene el permiso para que el proceso de cliente habilite la operación con privilegios.</span><span class="sxs-lookup"><span data-stu-id="87d99-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="87d99-114">Este paso solo es necesario si el proveedor es local para el cliente.</span><span class="sxs-lookup"><span data-stu-id="87d99-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="87d99-115">Si el cliente y el proveedor existen en el mismo equipo, el cliente debe habilitar específicamente la operación con privilegios mediante una de las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="87d99-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="87d99-116">Si el cliente es el propietario del proceso, el cliente puede usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para ajustar el token de proceso antes de llamar a WMI.</span><span class="sxs-lookup"><span data-stu-id="87d99-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="87d99-117">En este caso, no es necesario codificar más.</span><span class="sxs-lookup"><span data-stu-id="87d99-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="87d99-118">Si el cliente no puede tener acceso al token de cliente, el cliente puede usar el procedimiento siguiente para crear un token de subproceso y usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en ese token.</span><span class="sxs-lookup"><span data-stu-id="87d99-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="87d99-119">En el procedimiento siguiente se describe cómo crear un token de subproceso y usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en ese token.</span><span class="sxs-lookup"><span data-stu-id="87d99-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="87d99-120">**Para crear un token de subproceso y usar AdjustTokenPrivileges en ese token**</span><span class="sxs-lookup"><span data-stu-id="87d99-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="87d99-121">Cree una copia del token de proceso mediante una llamada a [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span><span class="sxs-lookup"><span data-stu-id="87d99-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="87d99-122">Recupere el token de subproceso recién creado llamando a [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="87d99-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="87d99-123">Habilite la operación con privilegios con una llamada a [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) en el nuevo token.</span><span class="sxs-lookup"><span data-stu-id="87d99-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="87d99-124">Obtener un puntero a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="87d99-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="87d99-125">Cloaking el puntero a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una llamada a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="87d99-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="87d99-126">Repita los pasos del 1 al 5 en cada llamada a WMI.</span><span class="sxs-lookup"><span data-stu-id="87d99-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="87d99-127">Debe repetir los pasos porque COM almacena en caché los tokens de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="87d99-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="87d99-128">El ejemplo de código de este tema requiere la siguiente \# instrucción include para compilar correctamente.</span><span class="sxs-lookup"><span data-stu-id="87d99-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="87d99-129">En el ejemplo de código siguiente se muestra cómo habilitar los privilegios en un equipo local.</span><span class="sxs-lookup"><span data-stu-id="87d99-129">The following code example shows how to enable privileges on a local machine.</span></span>


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



 

 
