---
description: Cada propiedad de control de inscripción de certificado es de lectura/escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables.
ms.assetid: e31dd6df-bc2a-401f-9343-a7dbb0f374bb
title: Uso de las propiedades de control de inscripción de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192ad4efd3d2438f800d4a3872a8cf1057ca9920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811227"
---
# <a name="using-the-certificate-enrollment-control-properties"></a><span data-ttu-id="11822-103">Uso de las propiedades de control de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="11822-103">Using the Certificate Enrollment Control Properties</span></span>

<span data-ttu-id="11822-104">Cada propiedad de control de inscripción de certificado es de lectura/escritura y tiene un valor predeterminado inicializado, así como un conjunto de valores aceptables.</span><span class="sxs-lookup"><span data-stu-id="11822-104">Each Certificate Enrollment Control property is read/write and has an initialized default as well as a set of acceptable values.</span></span> <span data-ttu-id="11822-105">Puede establecer una propiedad en cualquier valor de este conjunto para modificar el comportamiento de los métodos que usan la propiedad.</span><span class="sxs-lookup"><span data-stu-id="11822-105">You can set a property to any value within this set in order to modify the behavior of methods that use the property.</span></span> <span data-ttu-id="11822-106">Para obtener un comportamiento deseado, establezca la propiedad antes de llamar al método que utiliza el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="11822-106">To get a desired behavior, set the property before you call the method that uses that property's value.</span></span>

<span data-ttu-id="11822-107">Sin embargo, tenga en cuenta que después de llamar a los métodos siguientes</span><span class="sxs-lookup"><span data-stu-id="11822-107">Note, however, that after calling the following methods</span></span>

-   [<span data-ttu-id="11822-108">**acceptPKCS7**</span><span class="sxs-lookup"><span data-stu-id="11822-108">**acceptPKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptpkcs7)
-   [<span data-ttu-id="11822-109">**acceptFilePKCS7**</span><span class="sxs-lookup"><span data-stu-id="11822-109">**acceptFilePKCS7**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-acceptfilepkcs7)
-   [<span data-ttu-id="11822-110">**createPKCS10**</span><span class="sxs-lookup"><span data-stu-id="11822-110">**createPKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createpkcs10)
-   [<span data-ttu-id="11822-111">**createFilePKCS10**</span><span class="sxs-lookup"><span data-stu-id="11822-111">**createFilePKCS10**</span></span>](/windows/desktop/api/Xenroll/nf-xenroll-icenroll-createfilepkcs10)

<span data-ttu-id="11822-112">las siguientes propiedades están bloqueadas para restablecerse</span><span class="sxs-lookup"><span data-stu-id="11822-112">the following properties are blocked from being reset</span></span>

-   [<span data-ttu-id="11822-113">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="11822-113">**ProviderType**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providertype)
-   [<span data-ttu-id="11822-114">**Especificación**</span><span class="sxs-lookup"><span data-stu-id="11822-114">**KeySpec**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_keyspec)
-   [<span data-ttu-id="11822-115">**ProviderFlags**</span><span class="sxs-lookup"><span data-stu-id="11822-115">**ProviderFlags**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providerflags)
-   [<span data-ttu-id="11822-116">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="11822-116">**ContainerName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_containername)
-   [<span data-ttu-id="11822-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="11822-117">**ProviderName**</span></span>](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_providername)

<span data-ttu-id="11822-118">a menos que se llame al método [**ICEnroll4:: RESET**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) .</span><span class="sxs-lookup"><span data-stu-id="11822-118">unless the [**ICEnroll4::Reset**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll3-reset) method is called.</span></span>

<span data-ttu-id="11822-119">Para obtener información sobre las propiedades y los métodos individuales, vea los temas de referencia de esas propiedades y métodos en la [referencia de criptografía](cryptography-reference.md).</span><span class="sxs-lookup"><span data-stu-id="11822-119">For information about individual properties and methods, see the reference topics for those properties and methods in the [Cryptography Reference](cryptography-reference.md).</span></span>

<span data-ttu-id="11822-120">Las secciones siguientes contienen información específica del idioma para establecer y recuperar las propiedades del control de inscripción de certificados:</span><span class="sxs-lookup"><span data-stu-id="11822-120">The following sections contain language-specific information for setting and retrieving the Certificate Enrollment Control properties:</span></span>

-   [<span data-ttu-id="11822-121">Propiedades de control de inscripción de certificados en C++</span><span class="sxs-lookup"><span data-stu-id="11822-121">Certificate Enrollment Control Properties in C++</span></span>](certificate-enrollment-control-properties-in-c-.md)

 

 
