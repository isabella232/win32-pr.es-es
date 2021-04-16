---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670101"
---
# <a name="cert2spc"></a><span data-ttu-id="a39eb-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="a39eb-103">Cert2SPC</span></span>

<span data-ttu-id="a39eb-104">La herramienta Cert2SPC crea un [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) de prueba mediante el uso de [*certificados*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existentes.</span><span class="sxs-lookup"><span data-stu-id="a39eb-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="a39eb-105">Cert2SPC puede encapsular varios certificados X. 509 en un objeto de datos firmados [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a39eb-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="a39eb-106">La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a39eb-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="a39eb-107">Cert2SPC está disponible como parte de la Windows SDK, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="a39eb-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="a39eb-108">Esta herramienta solo se utiliza con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="a39eb-108">This tool is for test purposes only.</span></span> <span data-ttu-id="a39eb-109">Se obtiene un SPC válido de una [*entidad de certificación*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a39eb-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="a39eb-110">**Cert2SPC** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="a39eb-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="a39eb-111">*Salida. SPC*</span><span class="sxs-lookup"><span data-stu-id="a39eb-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39eb-112">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="a39eb-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="a39eb-113">Nombres de los certificados X. 509 que se van a incluir en el SPC.</span><span class="sxs-lookup"><span data-stu-id="a39eb-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="a39eb-114">Cada nombre de certificado termina con la extensión. cer.</span><span class="sxs-lookup"><span data-stu-id="a39eb-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="a39eb-115">*Salida. SPC*</span><span class="sxs-lookup"><span data-stu-id="a39eb-115">*Output.spc*</span></span>            | <span data-ttu-id="a39eb-116">Nombre del objeto PKCS \# 7 que contiene los certificados X. 509 que se van a crear.</span><span class="sxs-lookup"><span data-stu-id="a39eb-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="a39eb-117">El nombre del archivo de salida termina con la extensión. SPC.</span><span class="sxs-lookup"><span data-stu-id="a39eb-117">The output file name ends with the .spc extension.</span></span> |



 

 

 
