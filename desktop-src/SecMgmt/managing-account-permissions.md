---
description: LSA proporciona varias funciones a las que las aplicaciones pueden llamar para enumerar o establecer privilegios para cuentas de usuario, grupo y grupo local.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Administración de permisos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5424d43424b067bc4771bd687c287e05e195f3e807a2db64bebaed4ece049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894078"
---
# <a name="managing-account-permissions"></a>Administración de permisos de cuenta

LSA proporciona varias funciones a las que las aplicaciones pueden llamar para enumerar o establecer [*privilegios*](/windows/desktop/SecGloss/p-gly) para cuentas de usuario, grupo y grupo local.

Para poder administrar la información de la cuenta, la aplicación debe obtener un identificador para el objeto [**de**](policy-object.md) directiva local, como se muestra en [Apertura de un identificador de objeto de directiva](opening-a-policy-object-handle.md). Además, para enumerar o editar permisos para una [](/windows/desktop/SecGloss/s-gly) cuenta, debe tener el identificador de seguridad (SID) para esa cuenta. La aplicación puede encontrar un SID según el nombre de la cuenta, como se describe en Traducción entre nombres [y SID.](translating-between-names-and-sids.md)

Para acceder a todas las cuentas que tienen un permiso determinado, llame a [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Esta función rellena una matriz con los SID de todas las cuentas que tienen el permiso especificado.

Después de obtener el SID de una cuenta, puede modificar sus permisos. Llame [**a LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) para agregar permisos a la cuenta. Si la cuenta especificada no existe, **LsaAddAccountRights la** crea. Para quitar permisos de una cuenta, llame a [**LsaRemoveAccountRights.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights) Si quita todos los permisos de una cuenta, **LsaRemoveAccountRights** también elimina la cuenta.

La aplicación puede comprobar los permisos asignados actualmente a una cuenta llamando a [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Esta función rellena una matriz de estructuras [**\_ STRING UNICODE \_ LSA.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) Cada estructura contiene el nombre de un privilegio mantenido por la cuenta especificada.

En el ejemplo siguiente se agrega el permiso SeServiceLogonRight a una cuenta. En este ejemplo, la variable AccountSID especifica el SID de la cuenta. Para obtener más información sobre cómo buscar un SID de cuenta, vea [Translateing Between Names and SIDs](translating-between-names-and-sids.md).


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



En el ejemplo anterior, la función InitLsaString convierte una cadena [*Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura [**STRING UNICODE \_ \_ LSA.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) El código de esta función se muestra en [Using LSA Unicode Strings (Uso de cadenas Unicode LSA).](using-lsa-unicode-strings.md)

 

 
