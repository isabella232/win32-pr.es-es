---
title: Crear y registrar SPN para el servicio de sockets de Windows basado en SCP
description: En el ejemplo de código siguiente se muestra cómo crear y registrar los SPN de un servicio. Llame a este código desde el instalador del servicio después de llamar a CreateService y crear el punto de conexión de servicio (SCP) del servicio.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- entidad de seguridad de servicio de AD, que compone y registra SPN para un servicio de sockets de Windows basado en SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072368"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Crear y registrar SPN para el servicio de sockets de Windows basado en SCP

En el ejemplo de código siguiente se muestra cómo crear y registrar los SPN de un servicio. Llame a este código desde el instalador del servicio después de llamar a [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) y crear el punto de conexión de servicio (SCP) del servicio.

En el ejemplo de código siguiente se llama a las funciones de ejemplo **SpnCompose** y **SpnRegister** que componen y registran el SPN. Para obtener más información y el código fuente **de SpnCompose,** vea Crear los SPN para un servicio [con un SCP.](composing-the-spns-for-a-service-with-an-scp.md) Para obtener más información y el **código fuente de SpnRegister,** vea [Registrar los SPN para un servicio](registering-the-spns-for-a-service.md).

En este ejemplo se usa el nombre de clase de servicio y el nombre distintivo de su SCP para crear su nombre de entidad de seguridad de servicio. Para obtener más información y un ejemplo de código que muestra cómo el cliente se enlaza al SCP de servicio para recuperar estas cadenas de nombre, vea How [Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md). Tenga en cuenta que el código para crear un SPN varía según el tipo de servicio y los mecanismos usados para publicar el servicio.

El servicio registra su SPN almacen guardarlo en el atributo **servicePrincipalName** del objeto de cuenta del servicio en el directorio . Si el servicio se ejecuta en la cuenta LocalSystem en lugar de en una cuenta de servicio, registra su SPN en el objeto de la cuenta de equipo local en el directorio .


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



Puede usar código similar para anular el registro de los SPN cuando se desinstale el servicio. Especifique la operación **DS \_ SPN \_ DELETE \_ SPN \_ OP** en lugar de **DS \_ SPN \_ ADD \_ SPN \_ OP**.

 

 