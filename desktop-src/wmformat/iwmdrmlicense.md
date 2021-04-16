---
title: Interfaz IWMDRMLicense
description: La interfaz IWMDRMLicense representa una lista de una o más licencias.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Interfaz IWMDRMLicense formato de Windows Media
- Interfaz IWMDRMLicense formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487951"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="1917b-105">Interfaz IWMDRMLicense</span><span class="sxs-lookup"><span data-stu-id="1917b-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="1917b-106">La interfaz **IWMDRMLicense** representa una lista de una o más licencias.</span><span class="sxs-lookup"><span data-stu-id="1917b-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="1917b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1917b-107">Members</span></span>

<span data-ttu-id="1917b-108">La interfaz **IWMDRMLicense** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1917b-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1917b-109">**IWMDRMLicense** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1917b-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="1917b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1917b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1917b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1917b-111">Methods</span></span>

<span data-ttu-id="1917b-112">La interfaz **IWMDRMLicense** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1917b-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="1917b-113">Método</span><span class="sxs-lookup"><span data-stu-id="1917b-113">Method</span></span>                                                                                   | <span data-ttu-id="1917b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1917b-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1917b-115">**CanPersist**</span><span class="sxs-lookup"><span data-stu-id="1917b-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="1917b-116">Consulta si la licencia puede conservarse en un almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="1917b-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="1917b-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="1917b-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="1917b-118">Crea un objeto descifrador con la configuración de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="1917b-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="1917b-119">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="1917b-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="1917b-120">Crea un objeto de sistema de cifrado con los valores de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="1917b-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="1917b-121">**CreateSecureDecryptor**</span><span class="sxs-lookup"><span data-stu-id="1917b-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="1917b-122">Crea un objeto descifrador seguro.</span><span class="sxs-lookup"><span data-stu-id="1917b-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="1917b-123">El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.</span><span class="sxs-lookup"><span data-stu-id="1917b-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="1917b-124">**GetAnalogVideoRestrictionLevels**</span><span class="sxs-lookup"><span data-stu-id="1917b-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="1917b-125">Recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="1917b-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="1917b-126">**GetInclusionList**</span><span class="sxs-lookup"><span data-stu-id="1917b-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="1917b-127">Recupera la lista de inclusión completa para la licencia actual o la cadena de licencias.</span><span class="sxs-lookup"><span data-stu-id="1917b-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="1917b-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="1917b-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="1917b-129">Recupera la licencia como lenguaje de marcado extensible (XML) o los datos de los derechos multimedia extensibles (XMR).</span><span class="sxs-lookup"><span data-stu-id="1917b-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="1917b-130">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="1917b-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="1917b-131">Recupera una propiedad de la licencia actual.</span><span class="sxs-lookup"><span data-stu-id="1917b-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="1917b-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="1917b-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="1917b-133">Carga la información sobre la siguiente licencia de la lista.</span><span class="sxs-lookup"><span data-stu-id="1917b-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="1917b-134">**GetOutputProtectionLevels**</span><span class="sxs-lookup"><span data-stu-id="1917b-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="1917b-135">Recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.</span><span class="sxs-lookup"><span data-stu-id="1917b-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="1917b-136">**PersistLicense**</span><span class="sxs-lookup"><span data-stu-id="1917b-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="1917b-137">Guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.</span><span class="sxs-lookup"><span data-stu-id="1917b-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="1917b-138">**ResetEnumeration**</span><span class="sxs-lookup"><span data-stu-id="1917b-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="1917b-139">Restablece la lista de licencias a su estado original.</span><span class="sxs-lookup"><span data-stu-id="1917b-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="1917b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1917b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1917b-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="1917b-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

