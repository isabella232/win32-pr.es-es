---
title: Establecer permisos en operaciones de objetos secundarios
description: También se pueden conceder o denegar permisos, como crear elemento secundario y eliminar secundario, para operaciones en todos los subobjetos o subobjetos de una clase específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Establecer permisos en operaciones de objetos secundarios AD
- objetos AD, Child, establecimiento de permisos en operaciones de objetos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149163"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="a70b5-105">Establecer permisos en operaciones de objetos secundarios</span><span class="sxs-lookup"><span data-stu-id="a70b5-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="a70b5-106">También se pueden conceder o denegar permisos, como crear elemento secundario y eliminar secundario, para operaciones en todos los subobjetos o subobjetos de una clase específica.</span><span class="sxs-lookup"><span data-stu-id="a70b5-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="a70b5-107">El siguiente procedimiento se puede usar para establecer permisos para un tipo de subobjeto específico.</span><span class="sxs-lookup"><span data-stu-id="a70b5-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="a70b5-108">**Para establecer permisos para un tipo de subobjeto específico**</span><span class="sxs-lookup"><span data-stu-id="a70b5-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="a70b5-109">Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.</span><span class="sxs-lookup"><span data-stu-id="a70b5-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="a70b5-110">Establezca la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el GUID de la clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="a70b5-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="a70b5-111">Esta es la propiedad **schemaIDGUID** del objeto ClassSchema que define la clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="a70b5-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="a70b5-112">Si la propiedad **objecttype** es **null**, la ACE se aplica a los subobjetos de cualquier clase.</span><span class="sxs-lookup"><span data-stu-id="a70b5-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="a70b5-113">Establezca la propiedad [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **tipo de \_ objeto marca de ADS \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="a70b5-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="a70b5-114">Para obtener más información y un procedimiento para crear una ACE, vea [establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="a70b5-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="a70b5-115">Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que controla las operaciones de objetos secundarios, vea el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="a70b5-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 