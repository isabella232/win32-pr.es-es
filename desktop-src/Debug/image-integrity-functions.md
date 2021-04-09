---
description: Las funciones de integridad de la imagen administran el conjunto de certificados en un archivo de imagen.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Funciones de integridad de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080174"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="0c873-103">Funciones de integridad de la imagen</span><span class="sxs-lookup"><span data-stu-id="0c873-103">Image Integrity Functions</span></span>

<span data-ttu-id="0c873-104">Las funciones de integridad de la imagen administran el conjunto de certificados en un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="0c873-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="0c873-105">Se proporcionan rutinas para agregar, quitar y consultar certificados.</span><span class="sxs-lookup"><span data-stu-id="0c873-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="0c873-106">También hay una función disponible para obtener la secuencia de bytes de un archivo de imagen necesario para calcular una síntesis del mensaje del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="0c873-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="0c873-107">Esto es necesario para crear certificados de firma.</span><span class="sxs-lookup"><span data-stu-id="0c873-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="0c873-108">Todos los certificados de un archivo tienen un índice que puede cambiar a medida que se quitan los certificados.</span><span class="sxs-lookup"><span data-stu-id="0c873-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="0c873-109">Siempre se agregarán nuevos certificados "al final" de la lista de certificados existentes.</span><span class="sxs-lookup"><span data-stu-id="0c873-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="0c873-110">Es decir, se les asignarán índices que son mayores que cualquier índice actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="0c873-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="0c873-111">En general, una aplicación no debe suponer que un certificado determinado tiene el mismo índice que tenía la última vez que se hacía referencia a él.</span><span class="sxs-lookup"><span data-stu-id="0c873-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="0c873-112">**DigestFunction**</span><span class="sxs-lookup"><span data-stu-id="0c873-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="0c873-113">**ImageAddCertificate**</span><span class="sxs-lookup"><span data-stu-id="0c873-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="0c873-114">**ImageEnumerateCertificates**</span><span class="sxs-lookup"><span data-stu-id="0c873-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="0c873-115">**ImageGetCertificateData**</span><span class="sxs-lookup"><span data-stu-id="0c873-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="0c873-116">**ImageGetCertificateHeader**</span><span class="sxs-lookup"><span data-stu-id="0c873-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="0c873-117">**ImageGetDigestStream**</span><span class="sxs-lookup"><span data-stu-id="0c873-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="0c873-118">**ImageRemoveCertificate**</span><span class="sxs-lookup"><span data-stu-id="0c873-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



