---
description: La interfaz ICertSrvSetupKeyInformation define las siguientes propiedades.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propiedades de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910073"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="69d06-103">Propiedades de ICertSrvSetupKeyInformation</span><span class="sxs-lookup"><span data-stu-id="69d06-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="69d06-104">La interfaz [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="69d06-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="69d06-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69d06-105">Property</span></span>                                                                           | <span data-ttu-id="69d06-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="69d06-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d06-107">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="69d06-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="69d06-108">Obtiene o establece el nombre utilizado por el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) para generar, almacenar o tener acceso a la clave.</span><span class="sxs-lookup"><span data-stu-id="69d06-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="69d06-109">**Existing**</span><span class="sxs-lookup"><span data-stu-id="69d06-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="69d06-110">Obtiene o establece un valor que indica si la clave privada ya existe.</span><span class="sxs-lookup"><span data-stu-id="69d06-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="69d06-111">**ExistingCACertificate**</span><span class="sxs-lookup"><span data-stu-id="69d06-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="69d06-112">Obtiene o establece el valor binario que se ha codificado mediante [*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) y que es el valor binario del certificado de entidad de certificación que corresponde a una clave existente.</span><span class="sxs-lookup"><span data-stu-id="69d06-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="69d06-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="69d06-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="69d06-114">Obtiene o establece el nombre del algoritmo hash que se usa para firmar o comprobar el certificado de la entidad de certificación para la clave.</span><span class="sxs-lookup"><span data-stu-id="69d06-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="69d06-115">**Length**</span><span class="sxs-lookup"><span data-stu-id="69d06-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="69d06-116">Obtiene o establece la intensidad de la clave a uno de los valores admitidos por el CSP.</span><span class="sxs-lookup"><span data-stu-id="69d06-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="69d06-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="69d06-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="69d06-118">Obtiene o establece el nombre del CSP que se usa para generar o almacenar la clave privada.</span><span class="sxs-lookup"><span data-stu-id="69d06-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
