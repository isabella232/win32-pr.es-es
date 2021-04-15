---
description: La LSA proporciona varias funciones a las que las aplicaciones pueden llamar para enumerar o establecer los privilegios de las cuentas de usuario, grupo y grupo local.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Administrar permisos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497194"
---
# <a name="managing-account-permissions"></a>Administrar permisos de cuenta

La LSA proporciona varias funciones a las que las aplicaciones pueden llamar para enumerar o establecer los [*privilegios*](/windows/desktop/SecGloss/p-gly) de las cuentas de usuario, grupo y grupo local.

Antes de poder administrar la información de la cuenta, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, tal como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md). Además, para enumerar o Editar permisos para una cuenta, debe tener el identificador de [*seguridad*](/windows/desktop/SecGloss/s-gly) (SID) para esa cuenta. La aplicación puede localizar un SID dado el nombre de cuenta, como se describe en [traducir entre nombres y Sid](translating-between-names-and-sids.md).

Para tener acceso a todas las cuentas que tienen un permiso determinado, llame a [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Esta función rellena una matriz con los SID de todas las cuentas que tienen el permiso especificado.

Después de haber obtenido el SID de una cuenta, puede modificar sus permisos. Llame a [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) para agregar permisos a la cuenta. Si la cuenta especificada no existe, **LsaAddAccountRights** la crea. Para quitar permisos de una cuenta, llame a [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Si quita todos los permisos de una cuenta, **LsaRemoveAccountRights** también elimina la cuenta.

La aplicación puede comprobar los permisos asignados actualmente a una cuenta mediante una llamada a [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Esta función rellena una matriz de estructuras [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Cada estructura contiene el nombre de un privilegio mantenido por la cuenta especificada.

En el ejemplo siguiente se agrega el permiso SeServiceLogonRight a una cuenta. En este ejemplo, la variable AccountSID especifica el SID de la cuenta. Para obtener más información acerca de cómo buscar un SID de cuenta, consulte [traduciendo entre nombres y Sid](translating-between-names-and-sids.md).


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



En el ejemplo anterior, la función InitLsaString convierte una cadena [*Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).

 

 
