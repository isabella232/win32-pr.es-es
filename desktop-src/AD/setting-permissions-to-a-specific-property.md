---
title: Establecer permisos para una propiedad específica
description: Los permisos se pueden establecer para aplicarse a una propiedad específica de un objeto.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Establecer permisos para una propiedad específica AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077491"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="33379-104">Establecer permisos para una propiedad específica</span><span class="sxs-lookup"><span data-stu-id="33379-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="33379-105">Los permisos se pueden establecer para aplicarse a una propiedad específica de un objeto.</span><span class="sxs-lookup"><span data-stu-id="33379-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="33379-106">**Para establecer permisos que se aplican a una propiedad específica de un objeto**</span><span class="sxs-lookup"><span data-stu-id="33379-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="33379-107">Establezca la propiedad [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ right \_ DS \_ Read \_ prop** y/o **ADS \_ right \_ DS \_ Write \_ prop**.</span><span class="sxs-lookup"><span data-stu-id="33379-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="33379-108">Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.</span><span class="sxs-lookup"><span data-stu-id="33379-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="33379-109">Establezca la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="33379-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="33379-110">Es el **schemaIDGUID** del objeto **attributeSchema** que define la propiedad en el esquema.</span><span class="sxs-lookup"><span data-stu-id="33379-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="33379-111">El GUID debe especificarse como una cadena del formulario generado por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) en la biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="33379-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="33379-112">Establezca [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **\_ tipo de objeto de marca ADS \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="33379-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="33379-113">Para obtener más información sobre el **schemaIDGUID** de un atributo predefinido, vea [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="33379-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="33379-114">Para obtener más información y un ejemplo de código que se puede usar para recuperar un schemaIDGUID, vea [leer objetos attributeSchema y ClassSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="33379-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="33379-115">Para obtener más información sobre cómo crear una ACE, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="33379-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="33379-116">Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE específica de la propiedad, consulte el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="33379-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 