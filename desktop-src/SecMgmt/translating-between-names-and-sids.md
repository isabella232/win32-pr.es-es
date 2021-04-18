---
description: La autoridad de seguridad local (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de identificador de seguridad (SID) correspondientes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Traducir entre nombres y SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686669"
---
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="99344-103">Traducir entre nombres y SID</span><span class="sxs-lookup"><span data-stu-id="99344-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="99344-104">La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) proporciona funciones para traducir entre los nombres de usuario, grupo y grupo local y sus valores de [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="99344-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="99344-105">Para buscar nombres de cuenta, llame a la función [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) .</span><span class="sxs-lookup"><span data-stu-id="99344-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="99344-106">Esta función devuelve el SID como un par de índice de dominio o RID.</span><span class="sxs-lookup"><span data-stu-id="99344-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="99344-107">Para obtener el SID como un solo elemento, llame a la función [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) .</span><span class="sxs-lookup"><span data-stu-id="99344-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="99344-108">Para buscar los SID, llame a [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="99344-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="99344-109">Estas funciones pueden convertir la información de nombre y SID de cualquier dominio de confianza del sistema local.</span><span class="sxs-lookup"><span data-stu-id="99344-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="99344-110">Antes de poder traducir entre nombres de cuenta y Sid, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="99344-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="99344-111">En el siguiente ejemplo se busca el SID de una cuenta, dado el nombre de cuenta.</span><span class="sxs-lookup"><span data-stu-id="99344-111">The following example looks up the SID for an account, given the account name.</span></span>


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



<span data-ttu-id="99344-112">En el ejemplo anterior, la función **InitLsaString** convierte una cadena Unicode en una estructura [**de \_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="99344-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="99344-113">El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="99344-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="99344-114">Estas funciones de traducción se proporcionan principalmente para que las usen los editores de permisos para mostrar información de la [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="99344-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="99344-115">Un editor de permisos siempre debe llamar a estas funciones mediante el objeto de [**Directiva**](policy-object.md) del sistema en el que se encuentra el SID del [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) o el nombre.</span><span class="sxs-lookup"><span data-stu-id="99344-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="99344-116">Esto garantiza que se haga referencia al conjunto adecuado de dominios de confianza durante la traducción.</span><span class="sxs-lookup"><span data-stu-id="99344-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="99344-117">Windows Access Control también proporciona funciones que realizan traducciones entre Sid y nombres de cuenta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) y [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="99344-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="99344-118">Si su aplicación necesita buscar un nombre de cuenta o SID y no usa la funcionalidad de directiva LSA adicional, utilice las funciones de Access Control de Windows en lugar de las funciones de directiva de LSA.</span><span class="sxs-lookup"><span data-stu-id="99344-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="99344-119">Para obtener más información sobre estas funciones, vea [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="99344-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 
