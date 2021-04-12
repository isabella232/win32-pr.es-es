---
description: Los blobs opacos, también conocidos como OPAQUEKEYBLOBs, se usan para almacenar las claves de sesión en un formato específico del proveedor, como Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo de BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424036"
---
# <a name="opaque-blob-type"></a><span data-ttu-id="c9741-103">Tipo de BLOB opaco</span><span class="sxs-lookup"><span data-stu-id="c9741-103">Opaque BLOB Type</span></span>

<span data-ttu-id="c9741-104">Los [*blobs opacos*](../secgloss/o-gly.md), también conocidos como OPAQUEKEYBLOBs, se usan para almacenar [*las claves de sesión*](../secgloss/s-gly.md) en un formato específico del proveedor, como [*Schannel*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c9741-104">[*Opaque BLOBs*](../secgloss/o-gly.md), also known as OPAQUEKEYBLOBs, are used to store [*session keys*](../secgloss/s-gly.md) in a vendor-specific format, such as [*Schannel*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c9741-105">Contienen el material de clave base y toda la información de [*Estado*](../secgloss/s-gly.md) actual.</span><span class="sxs-lookup"><span data-stu-id="c9741-105">They contain the base key material and all current [*state*](../secgloss/s-gly.md) information.</span></span> <span data-ttu-id="c9741-106">Esto incluye información como el [*valor Salt*](../secgloss/s-gly.md), el [*Vector de inicialización*](../secgloss/i-gly.md)y la tabla de claves.</span><span class="sxs-lookup"><span data-stu-id="c9741-106">This includes information such as the [*salt value*](../secgloss/s-gly.md), the [*initialization vector*](../secgloss/i-gly.md), and the key table.</span></span> <span data-ttu-id="c9741-107">El formato de los blobs opacos no se publica.</span><span class="sxs-lookup"><span data-stu-id="c9741-107">The format of opaque BLOBs is unpublished.</span></span> <span data-ttu-id="c9741-108">Cada proveedor de CSP determina su propio formato de BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9741-108">Each CSP vendor determines its own BLOB format.</span></span>

<span data-ttu-id="c9741-109">Dado que una clave se exporta a un BLOB opaco en formato específico de CSP, solo se puede importar en el CSP desde el que se exportó originalmente.</span><span class="sxs-lookup"><span data-stu-id="c9741-109">Because a key is exported into an opaque BLOB in CSP-specific format, it can only be imported into the CSP from which it was originally exported.</span></span>

<span data-ttu-id="c9741-110">Cuando hay dos procesos implicados, cada [*proceso*](../secgloss/p-gly.md) llama a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independientemente.</span><span class="sxs-lookup"><span data-stu-id="c9741-110">When two processes are involved, each [*process*](../secgloss/p-gly.md) calls [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independently.</span></span> <span data-ttu-id="c9741-111">Cada proceso obtiene un identificador de un contenedor de claves.</span><span class="sxs-lookup"><span data-stu-id="c9741-111">Each process gets a handle to a key container.</span></span> <span data-ttu-id="c9741-112">Es posible que ambos procesos tengan identificadores al mismo contenedor de claves.</span><span class="sxs-lookup"><span data-stu-id="c9741-112">It is possible for both processes to have handles to the same key container.</span></span> <span data-ttu-id="c9741-113">Un proceso crea las claves y las exporta a los blobs opacos y, después, pasa los blobs al segundo proceso.</span><span class="sxs-lookup"><span data-stu-id="c9741-113">One process creates the keys and exports them into opaque BLOBs, then passes the BLOBs to the second process.</span></span> <span data-ttu-id="c9741-114">El segundo proceso importa las claves del BLOB en el [*contenedor de claves*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c9741-114">The second process imports the keys from the BLOB into its [*key container*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="c9741-115">Si un CSP de hardware no admite la exportación de claves, es posible que el BLOB solo contenga el índice de un registro de claves o algo similar.</span><span class="sxs-lookup"><span data-stu-id="c9741-115">If a hardware CSP does not support exporting keys, the BLOB might only contain the index of a key register, or something similar.</span></span> <span data-ttu-id="c9741-116">En este caso, se omite el resto del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c9741-116">In this case, the rest of the procedure is ignored.</span></span>

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
