---
description: En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar los mensajes de intercambio de información personal (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Funciones de intercambio de información personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688044"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="eacc5-103">Funciones de intercambio de información personal</span><span class="sxs-lookup"><span data-stu-id="eacc5-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="eacc5-104">En cada una de las secciones siguientes se describe una función exportada por Xenroll.dll para administrar los mensajes de intercambio de información personal (PFX).</span><span class="sxs-lookup"><span data-stu-id="eacc5-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="eacc5-105">En cada sección también se describe cómo usar CertEnroll.dll para reemplazar la función o se indica que no existe ninguna asignación entre las dos bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="eacc5-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="eacc5-106">createFilePFXWStr</span><span class="sxs-lookup"><span data-stu-id="eacc5-106">createFilePFXWStr</span></span>

<span data-ttu-id="eacc5-107">La función [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) de Xenroll.dll guarda una cadena de certificados y una [*clave privada*](/windows/desktop/SecGloss/p-gly) en un archivo con el formato PFX.</span><span class="sxs-lookup"><span data-stu-id="eacc5-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="eacc5-108">La biblioteca CertEnroll.dll no implementa directamente la funcionalidad para copiar el mensaje PFX en un archivo.</span><span class="sxs-lookup"><span data-stu-id="eacc5-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="eacc5-109">Sin embargo, puede usar el método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje pfx codificado y escribir una función personalizada para guardar el mensaje en un archivo.</span><span class="sxs-lookup"><span data-stu-id="eacc5-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="eacc5-110">createPFXWStr</span><span class="sxs-lookup"><span data-stu-id="eacc5-110">createPFXWStr</span></span>

<span data-ttu-id="eacc5-111">La función [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) de Xenroll.dll guarda una cadena de certificados y una clave privada en una cadena de formato PFX.</span><span class="sxs-lookup"><span data-stu-id="eacc5-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="eacc5-112">Puede usar el método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) en la interfaz [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) para crear un mensaje pfx codificado que contenga la cadena de certificados y la clave.</span><span class="sxs-lookup"><span data-stu-id="eacc5-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="eacc5-113">Puede especificar una contraseña, opciones de exportación y tipo de codificación.</span><span class="sxs-lookup"><span data-stu-id="eacc5-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="eacc5-114">Para recuperar una cadena que es equivalente a la devuelta por [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pase la \_ marca binaria de cadena de cifrado XCN \_ \_ en el parámetro *Encoding* del método [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .</span><span class="sxs-lookup"><span data-stu-id="eacc5-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eacc5-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eacc5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eacc5-116">Asignación Xenroll.dll a CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="eacc5-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="eacc5-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="eacc5-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
