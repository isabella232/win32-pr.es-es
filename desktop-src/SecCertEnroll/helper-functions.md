---
description: En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll. En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Funciones auxiliares (API de inscripción de certificados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361148"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="087bf-104">Funciones auxiliares (API de inscripción de certificados)</span><span class="sxs-lookup"><span data-stu-id="087bf-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="087bf-105">En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="087bf-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="087bf-106">En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="087bf-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="087bf-107">binaryBlobToString</span><span class="sxs-lookup"><span data-stu-id="087bf-107">binaryBlobToString</span></span>

<span data-ttu-id="087bf-108">La función [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) de Xenroll.dll convierte una matriz de bytes en una cadena.</span><span class="sxs-lookup"><span data-stu-id="087bf-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="087bf-109">Con CertEnroll.dll, puede llamar al método [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) en la interfaz [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="087bf-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="087bf-110">stringToBinaryBlob</span><span class="sxs-lookup"><span data-stu-id="087bf-110">stringToBinaryBlob</span></span>

<span data-ttu-id="087bf-111">La función [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) de Xenroll.dll convierte una cadena en una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="087bf-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="087bf-112">Con CertEnroll.dll, puede llamar al método [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) en la interfaz [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) .</span><span class="sxs-lookup"><span data-stu-id="087bf-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="087bf-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="087bf-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087bf-114">Asignación Xenroll.dll a CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="087bf-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="087bf-115">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="087bf-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
