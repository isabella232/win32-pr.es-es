---
description: Los siguientes tipos de datos se utilizan en las funciones, interfaces y objetos de criptografía.
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: Tipos de datos de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666411"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="1ebdf-103">Tipos de datos de criptografía</span><span class="sxs-lookup"><span data-stu-id="1ebdf-103">Cryptography Data Types</span></span>

<span data-ttu-id="1ebdf-104">Los siguientes tipos de datos se utilizan en las funciones, interfaces y objetos de criptografía.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="1ebdf-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1ebdf-105">Data type</span></span>                                                                      | <span data-ttu-id="1ebdf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ebdf-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ebdf-107">**identificador de ALG \_**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="1ebdf-108">Especifica los identificadores de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="1ebdf-109">**\_respuesta de \_ OCSP del servidor de HCERT \_**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="1ebdf-110">Representa un identificador de una respuesta de OCSP asociada con una cadena de certificados de servidor.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="1ebdf-111">**HCRYPTHASH**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="1ebdf-112">Especifica los identificadores de un [*objeto hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1ebdf-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="1ebdf-113">**HCRYPTKEY**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="1ebdf-114">Especifica los identificadores de las claves criptográficas.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="1ebdf-115">**HCRYPTOIDFUNCADDR**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="1ebdf-116">Representa un identificador de una función que se puede instalar mediante un [*identificador de objeto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="1ebdf-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="1ebdf-117">**HCRYPTOIDFUNCSET**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="1ebdf-118">Representa un identificador para un conjunto de funciones que se pueden instalar mediante un OID.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="1ebdf-119">**HCRYPTPROV \_ heredado**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="1ebdf-120">Se usa para reemplazar el tipo de datos [**HCRYPTPROV**](hcryptprov.md) en el que ya no se usa el tipo de datos **HCRYPTPROV** .</span><span class="sxs-lookup"><span data-stu-id="1ebdf-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="1ebdf-121">**\_identificador de clave HCRYPTPROV o \_ NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="1ebdf-122">Especifica un identificador para un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de CryptoAPI o un CSP de CNG.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="1ebdf-123">**HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="1ebdf-124">Especifica un identificador para un CSP de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="1ebdf-125">**identificador de KEYSVCC \_**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="1ebdf-126">Especifica los identificadores para el servicio de clave.</span><span class="sxs-lookup"><span data-stu-id="1ebdf-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
