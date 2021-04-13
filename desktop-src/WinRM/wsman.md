---
title: Objeto WSMan (WSManDisp. h)
description: Proporciona métodos y propiedades que se usan para crear una sesión, representada por un objeto de sesión.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de objeto WSMan
- Administración remota de Windows de objeto WSMan, descrito
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421985"
---
# <a name="wsman-object"></a><span data-ttu-id="6e566-105">WSMan (objeto)</span><span class="sxs-lookup"><span data-stu-id="6e566-105">WSMan object</span></span>

<span data-ttu-id="6e566-106">Proporciona métodos y propiedades que se usan para crear una sesión, representada por un objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="6e566-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="6e566-107">Cualquier operación de Administración remota de Windows requiere la creación de una [**sesión**](session.md) que se conecta a un equipo remoto, un [*controlador de administración de base*](windows-remote-management-glossary.md) (BMC) o el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6e566-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="6e566-108">Las operaciones incluyen la obtención, escritura, enumeración de datos o la invocación de métodos.</span><span class="sxs-lookup"><span data-stu-id="6e566-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="6e566-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e566-109">Members</span></span>

<span data-ttu-id="6e566-110">El objeto **WSMan** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6e566-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="6e566-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e566-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6e566-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e566-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6e566-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e566-113">Methods</span></span>

<span data-ttu-id="6e566-114">El objeto **WSMan** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6e566-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6e566-115">Método</span><span class="sxs-lookup"><span data-stu-id="6e566-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6e566-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e566-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-118">Crea un objeto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> que especifica el nombre de usuario y la contraseña que se usan al crear una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6e566-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-120">Crea un objeto <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> que puede especificar:</span><span class="sxs-lookup"><span data-stu-id="6e566-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="6e566-121">Ruta de acceso completa a un <a href="windows-remote-management-glossary.md"><em>recurso</em></a> o a un solo dato.</span><span class="sxs-lookup"><span data-stu-id="6e566-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="6e566-122">Un <a href="windows-remote-management-glossary.md"><em>selector</em></a> para una instancia específica de un recurso.</span><span class="sxs-lookup"><span data-stu-id="6e566-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="6e566-123"><a href="windows-remote-management-glossary.md"><em>Opción</em></a> que proporciona datos adicionales al proveedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e566-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-125">Crea un objeto de <a href="session.md"><strong>sesión</strong></a> que se puede usar para las operaciones de red subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="6e566-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-127">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeep</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-129">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-131">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagHierarchyShallow</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-133">Devuelve el valor de la constante de enumeración <strong>WSManFlagNonXmlText</strong> para su uso en el parámetro <em>Flags</em> del método <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6e566-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-135">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnEPR</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-137">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObject</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-139">Devuelve el valor de la marca de enumeración <strong>EnumerationFlagReturnObjectAndEPR</strong> para su uso en el parámetro <em>Flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-140"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-141">Devuelve una cadena con formato que contiene el texto de un número de error.</span><span class="sxs-lookup"><span data-stu-id="6e566-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-143">Devuelve el valor de la marca de autenticación <strong>WSManFlagCredUsernamePassword</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-145">Devuelve el valor de la marca de autenticación <strong>WSManFlagEnableSPNServerPort</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-147">Devuelve el valor de la marca de autenticación <strong>WSManFlagNoEncryption</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-149">Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCACheck</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-151">Devuelve el valor de la marca de autenticación <strong>WSManFlagSkipCNCheck</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-153">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseBasic</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-155">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseDigest</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-157">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseKerberos</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-159">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNegotiate</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="6e566-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-161">Devuelve el valor de la marca de autenticación <strong>WSManFlagUseNoAuthentication</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="6e566-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e566-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="6e566-163">Devuelve el valor de la marca de autenticación <strong>WSManFlagUTF8</strong> para su uso en el parámetro <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. createSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6e566-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="6e566-164">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e566-164">Properties</span></span>

<span data-ttu-id="6e566-165">El objeto **WSMan** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e566-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="6e566-166">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e566-166">Property</span></span>                                            | <span data-ttu-id="6e566-167">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6e566-167">Access type</span></span>          | <span data-ttu-id="6e566-168">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e566-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="6e566-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="6e566-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="6e566-170">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e566-170">Read-only</span></span><br/> | <span data-ttu-id="6e566-171">Obtiene la línea de comandos no procesada para el proceso de hospedaje actual.</span><span class="sxs-lookup"><span data-stu-id="6e566-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="6e566-172">**Error**</span><span class="sxs-lookup"><span data-stu-id="6e566-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="6e566-173">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e566-173">Read-only</span></span><br/> | <span data-ttu-id="6e566-174">Obtiene la información de error.</span><span class="sxs-lookup"><span data-stu-id="6e566-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="6e566-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e566-175">Remarks</span></span>

<span data-ttu-id="6e566-176">El objeto **WSMan** corresponde a las interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) y [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) .</span><span class="sxs-lookup"><span data-stu-id="6e566-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="6e566-177">**WSMan** es el único objeto que se puede crear directamente mediante [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6e566-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="6e566-178">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6e566-178">Examples</span></span>

<span data-ttu-id="6e566-179">En el ejemplo de código siguiente se muestra cómo crear una instancia de un objeto **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="6e566-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="6e566-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e566-180">Requirements</span></span>



| <span data-ttu-id="6e566-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e566-181">Requirement</span></span> | <span data-ttu-id="6e566-182">Value</span><span class="sxs-lookup"><span data-stu-id="6e566-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e566-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e566-183">Minimum supported client</span></span><br/> | <span data-ttu-id="6e566-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e566-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6e566-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e566-185">Minimum supported server</span></span><br/> | <span data-ttu-id="6e566-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e566-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6e566-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e566-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e566-188"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e566-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e566-189">IDL</span><span class="sxs-lookup"><span data-stu-id="6e566-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e566-190"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e566-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e566-191">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e566-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e566-192"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e566-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e566-193">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e566-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e566-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e566-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e566-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e566-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e566-196">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="6e566-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="6e566-197">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="6e566-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="6e566-198">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="6e566-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="6e566-199">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="6e566-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="6e566-200">Obtención de datos del equipo local</span><span class="sxs-lookup"><span data-stu-id="6e566-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="6e566-201">Obtención de datos de un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="6e566-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

