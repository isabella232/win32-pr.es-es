---
description: Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Crear archivos y catálogos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277150"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="39a8e-103">Crear archivos y catálogos firmados</span><span class="sxs-lookup"><span data-stu-id="39a8e-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="39a8e-104">Para firmar un archivo y crear un catálogo para él, primero debe tener un proceso para firmar archivos, un certificado y una clave pública.</span><span class="sxs-lookup"><span data-stu-id="39a8e-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="39a8e-105">**Para firmar un archivo y crear un catálogo**</span><span class="sxs-lookup"><span data-stu-id="39a8e-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="39a8e-106">Use [Pktextract.exe](pktextract-exe.md) para extraer el [*token de clave pública*](p-sbscs-gly.md) del archivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="39a8e-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="39a8e-107">El archivo de certificado debe estar presente en el mismo directorio que la utilidad.</span><span class="sxs-lookup"><span data-stu-id="39a8e-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="39a8e-108">Use el valor del token de clave pública para actualizar el atributo **PublicKeyToken** del elemento **assemblyIdentity** en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="39a8e-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="39a8e-109">Utilice [MT.exe](mt-exe.md) para generar valores hash de los archivos contenidos en el manifiesto del ensamblado y para crear el archivo de Descripción del catálogo (. CDF).</span><span class="sxs-lookup"><span data-stu-id="39a8e-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="39a8e-110">Use Makecat.exe con el. CDF generado para crear el catálogo de seguridad para el ensamblado.</span><span class="sxs-lookup"><span data-stu-id="39a8e-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="39a8e-111">Esta herramienta se incluye en la CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="39a8e-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="39a8e-112">Use la utilidad [SignTool](/windows/desktop/SecCrypto/signtool) para firmar el catálogo generado con el certificado usado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="39a8e-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="39a8e-113">El. CDF de los pasos 3 y 4 se puede eliminar una vez que se crea el catálogo.</span><span class="sxs-lookup"><span data-stu-id="39a8e-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="39a8e-114">Vea también el [ejemplo de firma de ensamblados](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="39a8e-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
