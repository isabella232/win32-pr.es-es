---
description: Se utiliza para configurar los componentes de CAPICOM.
title: Objeto de configuración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690588"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="dc849-103">Objeto de configuración (criptografía)</span><span class="sxs-lookup"><span data-stu-id="dc849-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="dc849-104">\[El objeto de **configuración** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="dc849-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="dc849-105">El objeto de **configuración** se utiliza para configurar los componentes de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="dc849-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="dc849-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc849-106">Members</span></span>

<span data-ttu-id="dc849-107">El objeto de **configuración** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc849-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="dc849-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc849-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc849-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc849-109">Properties</span></span>

<span data-ttu-id="dc849-110">El objeto de **configuración** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc849-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="dc849-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc849-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dc849-112">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="dc849-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dc849-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc849-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="dc849-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc849-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="dc849-115">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc849-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="dc849-116">Establece o recupera la ubicación de búsqueda de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc849-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="dc849-117">La ubicación inicial no se especifica de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dc849-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="dc849-118">Cuando no se especifica la ubicación, se busca en el catálogo global y, a continuación, se busca en el dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dc849-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="dc849-119">La búsqueda determina si el atributo de certificado de usuario está publicado en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="dc849-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="dc849-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc849-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="dc849-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc849-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="dc849-122">Establece o recupera un valor booleano que indica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente.</span><span class="sxs-lookup"><span data-stu-id="dc849-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dc849-123">Al establecer esta propiedad, no se deshabilitan las advertencias generadas antes de que se realice un uso de clave privada desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="dc849-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="dc849-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc849-124">Remarks</span></span>

<span data-ttu-id="dc849-125">Se puede crear el objeto de **configuración** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="dc849-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="dc849-126">El ProgID del objeto de **configuración** es CAPICOM. Configuración. 1.</span><span class="sxs-lookup"><span data-stu-id="dc849-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc849-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc849-127">Requirements</span></span>



| <span data-ttu-id="dc849-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc849-128">Requirement</span></span> | <span data-ttu-id="dc849-129">Value</span><span class="sxs-lookup"><span data-stu-id="dc849-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc849-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dc849-130">Redistributable</span></span><br/> | <span data-ttu-id="dc849-131">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc849-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dc849-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc849-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="dc849-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc849-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc849-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc849-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc849-135">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="dc849-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




