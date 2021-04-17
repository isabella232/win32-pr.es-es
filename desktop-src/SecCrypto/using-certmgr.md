---
description: Use CertMgr para ver certificados, CRL y CTL desde un archivo o un almacén de certificados, para copiar certificados en un almacén de certificados, para eliminar certificados de un almacén de certificados y para guardar certificados en archivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Usar CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666723"
---
# <a name="using-certmgr"></a><span data-ttu-id="823cd-103">Usar CertMgr</span><span class="sxs-lookup"><span data-stu-id="823cd-103">Using CertMgr</span></span>

<span data-ttu-id="823cd-104">[Certmgr](certmgr.md) se puede usar para ver [*certificados*](../secgloss/c-gly.md), [*listas de revocación de certificados*](../secgloss/c-gly.md) (CRL) y [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL) de un archivo o un almacén de certificados, para copiar certificados en un [*almacén*](../secgloss/c-gly.md)de certificados, eliminar certificados de un almacén de certificados y guardar certificados en archivos.</span><span class="sxs-lookup"><span data-stu-id="823cd-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="823cd-105">Cuando se usa [Certmgr](certmgr.md) sin opciones, aparece un asistente de Certmgr para guiar al usuario a través de la operación.</span><span class="sxs-lookup"><span data-stu-id="823cd-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="823cd-106">El archivo debe ser uno de los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="823cd-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="823cd-107">Una CTL codificada, una CRL o un archivo de certificado (se puede codificar en base 64)</span><span class="sxs-lookup"><span data-stu-id="823cd-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="823cd-108">Un \# archivo PKCS 7</span><span class="sxs-lookup"><span data-stu-id="823cd-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="823cd-109">Un archivo SPC</span><span class="sxs-lookup"><span data-stu-id="823cd-109">An SPC file</span></span>
-   <span data-ttu-id="823cd-110">Un documento firmado</span><span class="sxs-lookup"><span data-stu-id="823cd-110">A signed document</span></span>
-   <span data-ttu-id="823cd-111">Un storeFile serializado</span><span class="sxs-lookup"><span data-stu-id="823cd-111">A serialized storeFile</span></span>

<span data-ttu-id="823cd-112">En los ejemplos siguientes se usan los comandos de [Certmgr](certmgr.md) para realizar tareas comunes de certificado.</span><span class="sxs-lookup"><span data-stu-id="823cd-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="823cd-113">Vea los certificados, las CRL y las CTL de *archivos. ext*.</span><span class="sxs-lookup"><span data-stu-id="823cd-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="823cd-114">**Certmgr** *. ext*</span><span class="sxs-lookup"><span data-stu-id="823cd-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="823cd-115">Vea los certificados, las CRL y las CTL del almacén del sistema.</span><span class="sxs-lookup"><span data-stu-id="823cd-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="823cd-116">**Certmgr-s mi**</span><span class="sxs-lookup"><span data-stu-id="823cd-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="823cd-117">Copie todos los certificados, CRL y listas CTL de un archivo llamado archivo *. ext* en un archivo nuevo, denominado *NewFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="823cd-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="823cd-118">**Certmgr-Add-All-c** *archivo. ext* *NewFile. ext*</span><span class="sxs-lookup"><span data-stu-id="823cd-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="823cd-119">Copie todos los certificados, CRL y listas CTL del almacén del sistema MY en un archivo denominado *NewMyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="823cd-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="823cd-120">**Certmgr-Add-All-c-s mis** *NewMyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="823cd-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="823cd-121">Copie un certificado con el nombre común *mycert* en mi almacén del sistema en un archivo denominado *NewCert. cer*.</span><span class="sxs-lookup"><span data-stu-id="823cd-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="823cd-122">**Certmgr-Add-c-n** *mycert* **-s My** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="823cd-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="823cd-123">Elimine todos los certificados de mi almacén del sistema.</span><span class="sxs-lookup"><span data-stu-id="823cd-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="823cd-124">**Certmgr-del-todos-c-s mi**</span><span class="sxs-lookup"><span data-stu-id="823cd-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="823cd-125">Elimine todas las CTL del almacén del sistema MY y guarde el almacén resultante en un archivo denominado *NewStore. Str*.</span><span class="sxs-lookup"><span data-stu-id="823cd-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="823cd-126">**Certmgr-del-All-CTL-s My** *NewStore. Str*</span><span class="sxs-lookup"><span data-stu-id="823cd-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="823cd-127">Guardar, en un archivo denominado *NewCert. cer*, un certificado que es un certificado codificado [*X. 509*](../secgloss/x-gly.md) , que tiene el nombre común *mycert* y que se encuentra en el almacén de certificados raíz.</span><span class="sxs-lookup"><span data-stu-id="823cd-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="823cd-128">**Certmgr-Put-c-n** *mycert* **-s raíz** *NewCert. cer*</span><span class="sxs-lookup"><span data-stu-id="823cd-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="823cd-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="823cd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="823cd-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="823cd-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
