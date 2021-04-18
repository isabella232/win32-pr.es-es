---
title: Atributos de identificación de usuario
description: La identidad del usuario que solicita la autenticación se proporciona a los archivos dll de extensión de NPS en varios atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, identificación de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685769"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="e454b-104">Atributos de identificación de usuario</span><span class="sxs-lookup"><span data-stu-id="e454b-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="e454b-105">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e454b-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="e454b-106">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="e454b-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e454b-107">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="e454b-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="e454b-108">La identidad del usuario que solicita la autenticación se proporciona a los archivos dll de extensión de NPS en varios atributos diferentes.</span><span class="sxs-lookup"><span data-stu-id="e454b-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="e454b-109">**ratUserName**</span><span class="sxs-lookup"><span data-stu-id="e454b-109">**ratUserName**</span></span>
-   <span data-ttu-id="e454b-110">**ratStrippedUserName**</span><span class="sxs-lookup"><span data-stu-id="e454b-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="e454b-111">**ratFQUserName**</span><span class="sxs-lookup"><span data-stu-id="e454b-111">**ratFQUserName**</span></span>

<span data-ttu-id="e454b-112">Cada atributo proporciona la identidad del usuario en un formato diferente.</span><span class="sxs-lookup"><span data-stu-id="e454b-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="e454b-113">En general, los desarrolladores deben usar **ratStrippedUserName**.</span><span class="sxs-lookup"><span data-stu-id="e454b-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="e454b-114">Los usos de los atributos **ratUserName** y **ratFQUserName** son más especializados.</span><span class="sxs-lookup"><span data-stu-id="e454b-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="e454b-115">El atributo User-Password, **ratUserPassword**, ya se ha descifrado cuando se envía al archivo dll de extensión y se puede usar en ese formulario.</span><span class="sxs-lookup"><span data-stu-id="e454b-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="e454b-116">ratUserName</span><span class="sxs-lookup"><span data-stu-id="e454b-116">ratUserName</span></span>

<span data-ttu-id="e454b-117">El atributo **ratUserName** contiene el nombre que se envió realmente "a través de la conexión".</span><span class="sxs-lookup"><span data-stu-id="e454b-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="e454b-118">NPS no ha procesado ni validado de ningún modo el contenido de este atributo.</span><span class="sxs-lookup"><span data-stu-id="e454b-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="e454b-119">Es posible que este atributo no esté disponible en absoluto porque es posible que el usuario se haya identificado a través de un medio como el identificador del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e454b-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="e454b-120">Cuando se usa [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), si este atributo está disponible, solo está disponible en el punto de conexión del archivo dll de extensión de autenticación.</span><span class="sxs-lookup"><span data-stu-id="e454b-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="e454b-121">El atributo **ratUserName** no está disponible en el punto de conexión del archivo dll de extensión de autorización porque, en las dll de extensión de autorización, las funciones **RadiusExtensionProcess/ex** solo ven los atributos "salientes".</span><span class="sxs-lookup"><span data-stu-id="e454b-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="e454b-122">Cuando se usa [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), si este atributo está disponible, está disponible en el punto de conexión del archivo dll de extensión de autenticación y en el punto de conexión del archivo dll de la extensión de autorización.</span><span class="sxs-lookup"><span data-stu-id="e454b-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="e454b-123">ratStrippedUserName</span><span class="sxs-lookup"><span data-stu-id="e454b-123">ratStrippedUserName</span></span>

<span data-ttu-id="e454b-124">**RatStrippedUserName** es la identidad del usuario después de "eliminación de territorio".</span><span class="sxs-lookup"><span data-stu-id="e454b-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="e454b-125">Para obtener más información sobre la eliminación de territorios, vea el tema [nombres de dominio Kerberos](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) en http: \\ \\ technet2.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e454b-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="e454b-126">Este atributo puede estar presente en el punto de conexión del archivo DLL de extensión de autenticación, en el punto de conexión del archivo DLL de extensión de autorización o en ambos.</span><span class="sxs-lookup"><span data-stu-id="e454b-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="e454b-127">Se garantiza que este atributo tiene el formato:</span><span class="sxs-lookup"><span data-stu-id="e454b-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="e454b-128">*Dominio ***\\*** nombre de usuario*</span><span class="sxs-lookup"><span data-stu-id="e454b-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="e454b-129">Donde *dominio* es el nombre de dominio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="e454b-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="e454b-130">ratFQUserName</span><span class="sxs-lookup"><span data-stu-id="e454b-130">ratFQUserName</span></span>

<span data-ttu-id="e454b-131">El atributo **ratFQUserName** es el nombre de usuario "completo".</span><span class="sxs-lookup"><span data-stu-id="e454b-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="e454b-132">Este atributo puede estar presente en el punto de conexión del archivo DLL de extensión de autenticación, en el punto de conexión del archivo DLL de extensión de autorización o en ambos.</span><span class="sxs-lookup"><span data-stu-id="e454b-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="e454b-133">Sin embargo, el formato del atributo puede diferir entre los dos puntos de complemento.</span><span class="sxs-lookup"><span data-stu-id="e454b-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="e454b-134">En el punto de conexión del archivo DLL de extensión de autenticación, este atributo siempre tendrá el formato:</span><span class="sxs-lookup"><span data-stu-id="e454b-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="e454b-135">*Dominio ***\\*** nombre de usuario*</span><span class="sxs-lookup"><span data-stu-id="e454b-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="e454b-136">El formato del atributo **ratFQUserName** en el punto de conexión del archivo dll de extensión de autorización depende de si el usuario es un usuario Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e454b-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="e454b-137">Si el usuario es un usuario local, **ratFQUserName** tiene el mismo formato que para el punto de conexión del archivo dll de extensión de autenticación:</span><span class="sxs-lookup"><span data-stu-id="e454b-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="e454b-138">*Dominio ***\\*** nombre de usuario*</span><span class="sxs-lookup"><span data-stu-id="e454b-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="e454b-139">.</span><span class="sxs-lookup"><span data-stu-id="e454b-139">.</span></span>

-   <span data-ttu-id="e454b-140">Si el usuario es un usuario Active Directory, **ratFQUserName** puede contener el nombre del usuario en formato "canónico".</span><span class="sxs-lookup"><span data-stu-id="e454b-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="e454b-141">El formato canónico es el formato utilizado por el Active Directory para identificar al usuario.</span><span class="sxs-lookup"><span data-stu-id="e454b-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="e454b-142">Es la ruta de acceso desde la raíz del árbol de Active Directory e incluye la unidad organizativa (OU) del usuario.</span><span class="sxs-lookup"><span data-stu-id="e454b-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e454b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e454b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e454b-144">Configuración de los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="e454b-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="e454b-145">Invocar los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="e454b-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 