---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581983"
---
# <a name="cert2spc"></a><span data-ttu-id="53e64-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="53e64-103">Cert2SPC</span></span>

<span data-ttu-id="53e64-104">La herramienta Cert2SPC crea una prueba [*de Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) mediante certificados [*X.509*](../secgloss/x-gly.md) [*existentes.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="53e64-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="53e64-105">Cert2SPC puede encapsular varios certificados X.509 en un objeto de datos con firma [*PKCS \# 7.*](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="53e64-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="53e64-106">La herramienta se instala en la carpeta Bin de la ruta de \\ instalación de Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="53e64-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="53e64-107">Cert2SPC está disponible como parte del SDK Windows, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="53e64-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="53e64-108">Esta herramienta solo tiene fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="53e64-108">This tool is for test purposes only.</span></span> <span data-ttu-id="53e64-109">Se obtiene un SPC válido de una [*entidad de certificación.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="53e64-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="53e64-110">**Cert2SPC** *Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="53e64-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="53e64-111">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="53e64-111">*Output.spc*</span></span>

 



| <span data-ttu-id="53e64-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53e64-112">Parameters</span></span>              | <span data-ttu-id="53e64-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="53e64-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53e64-114">*Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="53e64-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="53e64-115">Nombres de los certificados X.509 que se incluirán en el SPC.</span><span class="sxs-lookup"><span data-stu-id="53e64-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="53e64-116">Cada nombre de certificado termina con la extensión .cer.</span><span class="sxs-lookup"><span data-stu-id="53e64-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="53e64-117">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="53e64-117">*Output.spc*</span></span>            | <span data-ttu-id="53e64-118">Nombre del objeto PKCS \# 7 que contiene los certificados X.509 que se crearán.</span><span class="sxs-lookup"><span data-stu-id="53e64-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="53e64-119">El nombre del archivo de salida termina con la extensión .spc.</span><span class="sxs-lookup"><span data-stu-id="53e64-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
