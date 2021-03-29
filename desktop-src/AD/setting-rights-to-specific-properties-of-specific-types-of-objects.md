---
title: Establecer derechos en propiedades específicas de tipos específicos de objetos
description: Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- establecer derechos en propiedades específicas de tipos específicos de objetos AD
- Active Directory, usar, seguridad, establecer derechos en propiedades específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487391"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="ee348-105">Establecer derechos en propiedades específicas de tipos específicos de objetos</span><span class="sxs-lookup"><span data-stu-id="ee348-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="ee348-106">Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración.</span><span class="sxs-lookup"><span data-stu-id="ee348-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="ee348-107">Puede establecer una ACE heredable de objeto específico de la propiedad para permitir que un usuario o grupo especificado lea o escriba un atributo específico en una clase especificada de objetos secundarios en un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ee348-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="ee348-108">Por ejemplo, puede establecer una ACE en una unidad organizativa (OU) para permitir que un grupo Lea y escriba el atributo de número de teléfono de todos los objetos de usuario en la unidad organizativa.</span><span class="sxs-lookup"><span data-stu-id="ee348-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="ee348-109">**Para establecer ACE que se puedan heredar del objeto específico de la propiedad**</span><span class="sxs-lookup"><span data-stu-id="ee348-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="ee348-110">Establezca [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.</span><span class="sxs-lookup"><span data-stu-id="ee348-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="ee348-111">Establezca [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** del atributo.</span><span class="sxs-lookup"><span data-stu-id="ee348-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="ee348-112">Por ejemplo, el **schemaIDGUID** del atributo **telephoneNumber** es {bf967a49-0de6-11d0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="ee348-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="ee348-113">Establezca [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACEFLAG \_ inherit \_ ACE**.</span><span class="sxs-lookup"><span data-stu-id="ee348-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="ee348-114">Establezca [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la clase de objeto que puede heredar la ACE.</span><span class="sxs-lookup"><span data-stu-id="ee348-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="ee348-115">Por ejemplo, el **schemaIDGUID** de la clase **User** es {bf967aba-0de6-11d0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="ee348-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="ee348-116">Establezca [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **\_ tipo de objeto de marca ADS \_ \_ \_ presente** y el **tipo de \_ \_ objeto heredado de marca de anuncios \_ \_ \_ presente**.</span><span class="sxs-lookup"><span data-stu-id="ee348-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee348-117">Establezca ad \_ ACEFLAG \_ inherit \_ ACE para que la ACE se herede.</span><span class="sxs-lookup"><span data-stu-id="ee348-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="ee348-118">Además, Set ADS \_ ACEFLAG \_ solo hereda \_ \_ ACE si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor en el que se especifica la ACE.</span><span class="sxs-lookup"><span data-stu-id="ee348-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="ee348-119">Si no se hace esto, la ACE también entrará en vigor en el contenedor y podrá conceder derechos inesperados.</span><span class="sxs-lookup"><span data-stu-id="ee348-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="ee348-120">Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 