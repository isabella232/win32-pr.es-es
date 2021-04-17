---
description: Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del valor de sal que se va a utilizar. El proveedor base establece un valor Salt mediante el \_ valor del parámetro sal de KP. El proveedor base siempre establece once bytes de valor Salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Especificar un valor Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669884"
---
# <a name="specifying-a-salt-value"></a><span data-ttu-id="1d58f-105">Especificar un valor Salt</span><span class="sxs-lookup"><span data-stu-id="1d58f-105">Specifying a Salt Value</span></span>

<span data-ttu-id="1d58f-106">Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del [*valor de sal*](../secgloss/s-gly.md) que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="1d58f-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="1d58f-107">El proveedor base establece un valor Salt mediante el \_ valor del parámetro sal de KP.</span><span class="sxs-lookup"><span data-stu-id="1d58f-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="1d58f-108">El proveedor base siempre establece once bytes de valor Salt.</span><span class="sxs-lookup"><span data-stu-id="1d58f-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="1d58f-109">El proveedor mejorado establece el valor Salt llamando a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con el \_ valor de parámetro PK sal \_ ex especificado y con el parámetro *pbData* que apunta a una estructura de [**\_ \_ BLOB de tipo entero de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) que contiene el valor Salt.</span><span class="sxs-lookup"><span data-stu-id="1d58f-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="1d58f-110">La longitud total de una [*clave simétrica*](../secgloss/s-gly.md) de proveedor mejorada y su valor Salt no puede ser superior a 128 bits.</span><span class="sxs-lookup"><span data-stu-id="1d58f-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="1d58f-111">\_Se sigue proporcionando sal de KP para la compatibilidad con versiones anteriores con el proveedor base.</span><span class="sxs-lookup"><span data-stu-id="1d58f-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="1d58f-112">Las aplicaciones más recientes deben usar el \_ valor del parámetro PK sal \_ ex.</span><span class="sxs-lookup"><span data-stu-id="1d58f-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="1d58f-113">En el ejemplo siguiente se establece un valor Salt.</span><span class="sxs-lookup"><span data-stu-id="1d58f-113">The following example sets a salt value.</span></span>


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
