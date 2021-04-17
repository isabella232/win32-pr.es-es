---
title: IDENTIFICADOR de clave y clave
description: IDENTIFICADOR de clave y clave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- Administración de derechos digitales (DRM), claves
- DRM (administración de derechos digitales), claves
- Administración de derechos digitales (DRM), KID
- DRM (administración de derechos digitales), KID
- IDENTIFICADOR de clave (KID)
- KID (identificador de clave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704635"
---
# <a name="key-and-key-id"></a><span data-ttu-id="7f24d-110">IDENTIFICADOR de clave y clave</span><span class="sxs-lookup"><span data-stu-id="7f24d-110">Key and Key ID</span></span>

<span data-ttu-id="7f24d-111">Al empaquetar un archivo, se usa una clave.</span><span class="sxs-lookup"><span data-stu-id="7f24d-111">When you package a file, you use a key.</span></span> <span data-ttu-id="7f24d-112">Una clave es un fragmento de datos que se usa en los algoritmos de cifrado que protegen el contenido.</span><span class="sxs-lookup"><span data-stu-id="7f24d-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="7f24d-113">Hay dos partes en cada clave: una inicialización de clave de licencia y un identificador de clave (a menudo abreviado como KID).</span><span class="sxs-lookup"><span data-stu-id="7f24d-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="7f24d-114">El identificador de clave es público y se almacena en el encabezado de archivo como una manera de identificar la clave necesaria para descifrar el archivo.</span><span class="sxs-lookup"><span data-stu-id="7f24d-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="7f24d-115">La inicialización de la clave de licencia es un valor secreto que debe compartir el Empaquetador de contenido y el emisor de la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f24d-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="7f24d-116">Un identificador de clave identifica el contenido protegido desde la perspectiva de la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f24d-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="7f24d-117">Aunque puede usar el mismo identificador de clave para varios archivos, se recomienda usar siempre un identificador de clave único para cada fragmento de contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="7f24d-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="7f24d-118">Muchos de los métodos descritos en esta documentación usan cadenas de identificador de clave para seleccionar licencias.</span><span class="sxs-lookup"><span data-stu-id="7f24d-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="7f24d-119">Estas cadenas contienen el identificador de clave codificado en Base64.</span><span class="sxs-lookup"><span data-stu-id="7f24d-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f24d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f24d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f24d-121">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="7f24d-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




