---
description: Si usa la API de scripting para WMI, puede establecer privilegios de seguridad específicos.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Ejecutar operaciones con privilegios mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156821"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="f6314-103">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="f6314-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="f6314-104">Si usa la API de scripting para WMI, puede establecer privilegios de seguridad específicos.</span><span class="sxs-lookup"><span data-stu-id="f6314-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="f6314-105">Por ejemplo, puede establecer los privilegios de seguridad para solicitar un apagado del sistema operativo o para examinar el registro de eventos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f6314-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="f6314-106">Para obtener más información, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="f6314-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="f6314-107">Solo tiene que establecer privilegios cuando tenga acceso a WMI en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f6314-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="f6314-108">Cuando se tiene acceso a un host remoto, COM RPC establece automáticamente los privilegios.</span><span class="sxs-lookup"><span data-stu-id="f6314-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="f6314-109">Para determinar todos los privilegios necesarios, consulte la documentación de las clases WMI específicas a las que desea obtener acceso, como por ejemplo, [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="f6314-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="f6314-110">Para obtener más información, consulte [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="f6314-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="f6314-111">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="f6314-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="f6314-112">Establecer un privilegio desde el objeto de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="f6314-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="f6314-113">Establecer un privilegio como parte de un moniker</span><span class="sxs-lookup"><span data-stu-id="f6314-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="f6314-114">Revocar y restablecer privilegios</span><span class="sxs-lookup"><span data-stu-id="f6314-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="f6314-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6314-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="f6314-116">Establecer un privilegio desde el objeto de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="f6314-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="f6314-117">Utilice el procedimiento siguiente para establecer privilegios de seguridad en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6314-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="f6314-118">**Para establecer privilegios en Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="f6314-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="f6314-119">Cree un objeto de tipo [**SWbemLocator**](swbemlocator.md).</span><span class="sxs-lookup"><span data-stu-id="f6314-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="f6314-120">Agregue el nuevo privilegio al objeto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="f6314-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="f6314-121">El objeto de [**seguridad \_**](swbemlocator-security-.md) contiene una colección [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="f6314-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="f6314-122">Los objetos del conjunto son objetos [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="f6314-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="f6314-123">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="f6314-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="f6314-124">Inicie sesión en WMI y recupere un objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="f6314-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="f6314-125">El objeto [**SWbemServices**](swbemservices.md) hereda el privilegio que se establece en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="f6314-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="f6314-126">También puede establecer un privilegio mediante el método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="f6314-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="f6314-127">Establecer un privilegio como parte de un moniker</span><span class="sxs-lookup"><span data-stu-id="f6314-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="f6314-128">Puede establecer un privilegio como parte de un moniker.</span><span class="sxs-lookup"><span data-stu-id="f6314-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="f6314-129">En el ejemplo siguiente se muestra cómo agregar un privilegio de depuración a un moniker.</span><span class="sxs-lookup"><span data-stu-id="f6314-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="f6314-130">Revocar y restablecer privilegios</span><span class="sxs-lookup"><span data-stu-id="f6314-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="f6314-131">En el ejemplo siguiente se muestra cómo establecer el privilegio **SeDebugPrivilege** y revocar el privilegio **SeRemoteShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="f6314-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="f6314-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6314-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6314-133">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="f6314-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="f6314-134">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="f6314-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
