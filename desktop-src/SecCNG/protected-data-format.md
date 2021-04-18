---
description: Los datos protegidos se almacenan como un BLOB con codificación ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Formato de datos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156145"
---
# <a name="protected-data-format"></a><span data-ttu-id="c559b-103">Formato de datos protegidos</span><span class="sxs-lookup"><span data-stu-id="c559b-103">Protected Data Format</span></span>

<span data-ttu-id="c559b-104">Los datos protegidos se almacenan como un BLOB con codificación ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="c559b-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="c559b-105">Los datos tienen el formato CMS (sintaxis de mensajes de certificado).</span><span class="sxs-lookup"><span data-stu-id="c559b-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="c559b-106">La envoltura digital contiene contenido cifrado, información de destinatarios que contiene una clave de cifrado de contenido cifrada (CEK) y un encabezado que contiene información sobre el contenido, incluida la cadena de regla del descriptor de protección sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="c559b-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="c559b-107">Esto se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c559b-107">This is shown by the following diagram.</span></span>

![datos con doble cifrado protegidos](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="c559b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c559b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c559b-110">DPAPI DE CNG</span><span class="sxs-lookup"><span data-stu-id="c559b-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="c559b-111">Descriptores de protección</span><span class="sxs-lookup"><span data-stu-id="c559b-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="c559b-112">Proveedores de protección</span><span class="sxs-lookup"><span data-stu-id="c559b-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



