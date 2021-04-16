---
description: Las siguientes funciones se encuentran entre las funciones de CryptoAPI que se pueden extender.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Crear la nueva funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541006"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="a82c1-103">Crear la nueva funcionalidad</span><span class="sxs-lookup"><span data-stu-id="a82c1-103">Creating the New Functionality</span></span>

<span data-ttu-id="a82c1-104">Las siguientes funciones se encuentran entre las funciones de CryptoAPI que se pueden extender.</span><span class="sxs-lookup"><span data-stu-id="a82c1-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="a82c1-105">Función CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="a82c1-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="a82c1-106">Definición de nombre de función OID</span><span class="sxs-lookup"><span data-stu-id="a82c1-106">OID function name define</span></span>                         | <span data-ttu-id="a82c1-107">Cadena de nombre de función OID</span><span class="sxs-lookup"><span data-stu-id="a82c1-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="a82c1-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="a82c1-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="a82c1-109">CRYPT \_ OID \_ encode \_ Object \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="a82c1-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="a82c1-110">"CryptDllEncodeObject"</span><span class="sxs-lookup"><span data-stu-id="a82c1-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="a82c1-111">**CryptDecodeObject**</span><span class="sxs-lookup"><span data-stu-id="a82c1-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="a82c1-112">CRYPT \_ OID \_ descodificar \_ objeto \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="a82c1-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="a82c1-113">"CryptDllDecodeObject"</span><span class="sxs-lookup"><span data-stu-id="a82c1-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="a82c1-114">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="a82c1-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="a82c1-115">CIFRAdo de \_ almacenamiento abierto de OID de CRYPT \_ \_ \_ \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="a82c1-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="a82c1-116">"CertDllOpenStoreProv"</span><span class="sxs-lookup"><span data-stu-id="a82c1-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="a82c1-117">**CertVerifyCTLUsage**</span><span class="sxs-lookup"><span data-stu-id="a82c1-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="a82c1-118">CIFRAr \_ OID \_ comprobar \_ CTL \_ uso \_ FUNC</span><span class="sxs-lookup"><span data-stu-id="a82c1-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="a82c1-119">"CertDllVerifyCTLUsage"</span><span class="sxs-lookup"><span data-stu-id="a82c1-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="a82c1-120">**CertVerifyRevocation**</span><span class="sxs-lookup"><span data-stu-id="a82c1-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="a82c1-121">CIFRAr \_ OID \_ comprobar la \_ revocación \_ funci</span><span class="sxs-lookup"><span data-stu-id="a82c1-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="a82c1-122">"CertDllVerifyRevocation"</span><span class="sxs-lookup"><span data-stu-id="a82c1-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="a82c1-123">En el uso normal con un OID y un tipo de codificación existentes, se utiliza el código de la función CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a82c1-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="a82c1-124">Si se llama a una de estas funciones con un OID y un tipo de codificación que el código de la función CryptoAPI no estaba diseñado para controlar, se debe crear una nueva función que contenga la nueva funcionalidad en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="a82c1-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="a82c1-125">Ese archivo DLL debe estar registrado en el registro o instalado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="a82c1-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="a82c1-126">Cuando se llama a una de las funciones enumeradas con el OID y el tipo de codificación recién designados, se usa el código del nuevo archivo DLL en lugar del código proporcionado como parte de la función CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a82c1-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="a82c1-127">El nombre de la función recién desarrollada puede ser el nombre que aparece en "cadena de nombre de función OID" en la tabla anterior o se puede proporcionar un nombre diferente cuando se registra el nuevo código de función.</span><span class="sxs-lookup"><span data-stu-id="a82c1-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="a82c1-128">La nueva función debe usar un prototipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="a82c1-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="a82c1-129">En todos los casos excepto [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), este prototipo es el mismo que el de la función CryptoAPI que llama a la nueva función.</span><span class="sxs-lookup"><span data-stu-id="a82c1-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="a82c1-130">En el caso de **CertOpenStore** , el prototipo es como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a82c1-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="a82c1-131">Si los prototipos no coinciden, la pila del sistema estará dañada.</span><span class="sxs-lookup"><span data-stu-id="a82c1-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="a82c1-132">Además de proporcionar el código para la nueva función en un archivo DLL, la extensión de la funcionalidad de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requiere una definición de tipo para la nueva estructura de datos de C que se va a colocar en un archivo de encabezado incluido al compilar el programa del usuario.</span><span class="sxs-lookup"><span data-stu-id="a82c1-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




