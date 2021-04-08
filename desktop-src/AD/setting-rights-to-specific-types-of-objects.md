---
title: Establecer derechos en tipos específicos de objetos
description: En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede ser heredada por una clase específica de objetos.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- establecer derechos en tipos de objetos AD
- objetos AD, establecer derechos
- Active Directory, usar, seguridad, establecer derechos en tipos de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995058"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="6ea3a-106">Establecer derechos en tipos específicos de objetos</span><span class="sxs-lookup"><span data-stu-id="6ea3a-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="6ea3a-107">En el procedimiento siguiente se muestra cómo establecer una ACE que solo puede ser heredada por una clase específica de objetos.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="6ea3a-108">**Para establecer una ACE que solo puede ser heredada por una clase específica de objetos**</span><span class="sxs-lookup"><span data-stu-id="6ea3a-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="6ea3a-109">Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="6ea3a-110">Establezca la propiedad [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para incluir la \_ marca ADS ACEFLAG \_ inherit \_ ACE.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="6ea3a-111">Establezca la propiedad [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la clase de objeto que puede heredar la ACE.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="6ea3a-112">Establezca la propiedad [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **tipo de \_ \_ objeto heredado marca de ADS \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ea3a-113">Establezca **ad \_ ACEFLAG \_ inherit \_ ACE** para que la ACE se herede.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="6ea3a-114">Además, si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor en el que se especifica la ACE, debe establecer la **\_ ACE ACEFLAG de \_ \_ \_ solo heredar** .</span><span class="sxs-lookup"><span data-stu-id="6ea3a-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="6ea3a-115">Si no se hace esto, la ACE también entrará en vigor en el contenedor y podrá conceder derechos no deseados.</span><span class="sxs-lookup"><span data-stu-id="6ea3a-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="6ea3a-116">Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="6ea3a-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 