---
description: Un certificado X.509 versión 2 contiene los campos básicos definidos en la versión 1 y, además, agrega los siguientes campos.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Campos de la versión 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275179"
---
# <a name="version-2-fields"></a><span data-ttu-id="28a58-103">Campos de la versión 2</span><span class="sxs-lookup"><span data-stu-id="28a58-103">Version 2 Fields</span></span>

<span data-ttu-id="28a58-104">Un certificado X.509 versión 2 contiene los campos básicos definidos en la versión 1 y, además, agrega los siguientes campos.</span><span class="sxs-lookup"><span data-stu-id="28a58-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="28a58-105">Identificador único de emisor</span><span class="sxs-lookup"><span data-stu-id="28a58-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="28a58-106">Contiene un valor único que se puede utilizar para hacer que el nombre X.500 de la CA no sea ambiguo si lo reutilizan distintas entidades a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="28a58-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="28a58-107">Identificador único de firmante</span><span class="sxs-lookup"><span data-stu-id="28a58-107">Subject Unique Identifier</span></span>

<span data-ttu-id="28a58-108">Contiene un valor único que se puede utilizar para hacer que el nombre X.500 del firmante del certificado no sea ambiguo si lo reutilizan distintas entidades a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="28a58-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="28a58-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28a58-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28a58-110">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="28a58-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="28a58-111">Extensiones de la versión 3</span><span class="sxs-lookup"><span data-stu-id="28a58-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="28a58-112">Certificados de clave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="28a58-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



