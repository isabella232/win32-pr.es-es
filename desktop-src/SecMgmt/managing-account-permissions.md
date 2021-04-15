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
# <a name="managing-account-permissions"></a><span data-ttu-id="55268-103">Administrar permisos de cuenta</span><span class="sxs-lookup"><span data-stu-id="55268-103">Managing Account Permissions</span></span>

<span data-ttu-id="55268-104">La LSA proporciona varias funciones a las que las aplicaciones pueden llamar para enumerar o establecer los [*privilegios*](/windows/desktop/SecGloss/p-gly) de las cuentas de usuario, grupo y grupo local.</span><span class="sxs-lookup"><span data-stu-id="55268-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="55268-105">Antes de poder administrar la información de la cuenta, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, tal como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="55268-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="55268-106">Además, para enumerar o Editar permisos para una cuenta, debe tener el identificador de [*seguridad*](/windows/desktop/SecGloss/s-gly) (SID) para esa cuenta.</span><span class="sxs-lookup"><span data-stu-id="55268-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="55268-107">La aplicación puede localizar un SID dado el nombre de cuenta, como se describe en [traducir entre nombres y Sid](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="55268-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="55268-108">Para tener acceso a todas las cuentas que tienen un permiso determinado, llame a [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span><span class="sxs-lookup"><span data-stu-id="55268-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="55268-109">Esta función rellena una matriz con los SID de todas las cuentas que tienen el permiso especificado.</span><span class="sxs-lookup"><span data-stu-id="55268-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="55268-110">Después de haber obtenido el SID de una cuenta, puede modificar sus permisos.</span><span class="sxs-lookup"><span data-stu-id="55268-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="55268-111">Llame a [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) para agregar permisos a la cuenta.</span><span class="sxs-lookup"><span data-stu-id="55268-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="55268-112">Si la cuenta especificada no existe, **LsaAddAccountRights** la crea.</span><span class="sxs-lookup"><span data-stu-id="55268-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="55268-113">Para quitar permisos de una cuenta, llame a [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="55268-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="55268-114">Si quita todos los permisos de una cuenta, **LsaRemoveAccountRights** también elimina la cuenta.</span><span class="sxs-lookup"><span data-stu-id="55268-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="55268-115">La aplicación puede comprobar los permisos asignados actualmente a una cuenta mediante una llamada a [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span><span class="sxs-lookup"><span data-stu-id="55268-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="55268-116">Esta función rellena una matriz de estructuras [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="55268-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="55268-117">Cada estructura contiene el nombre de un privilegio mantenido por la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="55268-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="55268-118">En el ejemplo siguiente se agrega el permiso SeServiceLogonRight a una cuenta.</span><span class="sxs-lookup"><span data-stu-id="55268-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="55268-119">En este ejemplo, la variable AccountSID especifica el SID de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="55268-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="55268-120">Para obtener más información acerca de cómo buscar un SID de cuenta, consulte [traduciendo entre nombres y Sid](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="55268-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


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



<span data-ttu-id="55268-121">En el ejemplo anterior, la función InitLsaString convierte una cadena [*Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="55268-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="55268-122">El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="55268-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
