---
title: Creación y registro de SPN para el servicio Windows Sockets basados en SCP
description: En el ejemplo de código siguiente se muestra cómo crear y registrar los SPN para un servicio. Llame a este código desde el instalador de servicio después de llamar a CreateService y crear el punto de conexión de servicio (SCP) del servicio.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- nombres de entidad de seguridad de servicio AD, creación y registro de SPN para un servicio de Windows Sockets basado en SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789615"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Creación y registro de SPN para el servicio Windows Sockets basados en SCP

En el ejemplo de código siguiente se muestra cómo crear y registrar los SPN para un servicio. Llame a este código desde el instalador de servicio después de llamar a [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) y crear el punto de conexión de servicio (SCP) del servicio.

En el ejemplo de código siguiente se llama a las funciones de ejemplo **SpnCompose** y **SpnRegister** que componen y registran el SPN. Para obtener más información y el código fuente de **SpnCompose** , consulte [creación de SPN para un servicio con un SCP](composing-the-spns-for-a-service-with-an-scp.md). Para obtener más información y el código fuente de **SpnRegister** , consulte [registrar los SPN para un servicio](registering-the-spns-for-a-service.md).

En este ejemplo se usa el nombre de la clase de servicio y el nombre distintivo de su SCP para crear su nombre de entidad de seguridad de servicio. Para obtener más información y un ejemplo de código que muestra cómo el cliente se enlaza al SCP de servicio para recuperar estas cadenas de nombre, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md). Tenga en cuenta que el código para crear un SPN varía en función del tipo de servicio y de los mecanismos utilizados para publicar el servicio.

El servicio registra su SPN almacenándolos en el atributo **ServicePrincipalName** del objeto de cuenta del servicio en el directorio. Si el servicio se ejecuta bajo la cuenta LocalSystem en lugar de en una cuenta de servicio, registra su SPN en el objeto de la cuenta de equipo local en el directorio.


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



Puede usar código similar para anular el registro de los SPN cuando se desinstale el servicio. Especifique la operación de **\_ \_ \_ \_ OP** SPN de eliminación SPN de DS en lugar de SPN de **DS \_ \_ agregar \_ SPN \_ OP**.

 

 