---
description: La Directiva de LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Almacenar datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423767"
---
# <a name="storing-private-data"></a><span data-ttu-id="362a9-103">Almacenar datos privados</span><span class="sxs-lookup"><span data-stu-id="362a9-103">Storing Private Data</span></span>

<span data-ttu-id="362a9-104">La Directiva de LSA proporciona dos funciones que puede usar para establecer y recuperar datos privados.</span><span class="sxs-lookup"><span data-stu-id="362a9-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="362a9-105">Estos datos se almacenan como una cadena cifrada en el registro.</span><span class="sxs-lookup"><span data-stu-id="362a9-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="362a9-106">Por ejemplo, puede utilizar estas funciones para almacenar contraseñas de cuentas de servidor y otra información confidencial.</span><span class="sxs-lookup"><span data-stu-id="362a9-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="362a9-107">Llame a la función [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) para almacenar y cifrar los datos privados.</span><span class="sxs-lookup"><span data-stu-id="362a9-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="362a9-108">Como se describe en [Private Data Object](private-data-object.md), los objetos de datos privados incluyen tres tipos especializados: local, global y Machine.</span><span class="sxs-lookup"><span data-stu-id="362a9-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="362a9-109">Para crear un objeto especializado, agregue un prefijo al nombre de clave que se pasa a **LsaStorePrivateData**: "L $" para los objetos locales, "G $" para los objetos globales y "M $" para los objetos de equipo.</span><span class="sxs-lookup"><span data-stu-id="362a9-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="362a9-110">Si no va a crear uno de estos tipos especializados, no es necesario especificar un prefijo de nombre de clave.</span><span class="sxs-lookup"><span data-stu-id="362a9-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="362a9-111">Para recuperar y descodificar los datos privados almacenados previamente, llame a [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span><span class="sxs-lookup"><span data-stu-id="362a9-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="362a9-112">Tenga en cuenta que no puede recuperar objetos de datos privados del equipo; los objetos de equipo solo se pueden recuperar mediante el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="362a9-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="362a9-113">Antes de poder almacenar o recuperar datos privados, la aplicación debe obtener un identificador para el objeto de [**Directiva**](policy-object.md) local, como se muestra en [abrir un identificador de objeto de directiva](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="362a9-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="362a9-114">En el ejemplo siguiente se crea un objeto de datos privado local.</span><span class="sxs-lookup"><span data-stu-id="362a9-114">The following example creates a local private data object.</span></span> <span data-ttu-id="362a9-115">Tenga en cuenta que la función InitLsaString convierte una cadena [*Unicode*](/windows/desktop/SecGloss/u-gly) en una estructura de [**\_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="362a9-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="362a9-116">El código de esta función se muestra en [mediante cadenas de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="362a9-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="362a9-117">Los datos almacenados por la función [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) no están totalmente protegidos.</span><span class="sxs-lookup"><span data-stu-id="362a9-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="362a9-118">La clave, sin embargo, tiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que permite que solo el creador y los administradores lean los datos.</span><span class="sxs-lookup"><span data-stu-id="362a9-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 
