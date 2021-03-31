---
description: La propiedad AuthenticationLevel es un entero que define el nivel de autenticación COM que se asigna a este objeto.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Propiedad SWbemSecurity. AuthenticationLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360541"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="52757-103">Propiedad SWbemSecurity. AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="52757-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="52757-104">La propiedad **AuthenticationLevel** es un entero que define el nivel de autenticación com que se asigna a este objeto.</span><span class="sxs-lookup"><span data-stu-id="52757-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="52757-105">Esta configuración determina cómo se protege la información enviada desde WMI.</span><span class="sxs-lookup"><span data-stu-id="52757-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="52757-106">Para obtener más información acerca de los niveles de autenticación, vea [establecer la \_ seguridad de \_ procesos de aplicación cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="52757-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="52757-107">En general, no es necesario establecer el nivel de autenticación al realizar llamadas a la API de WMI.</span><span class="sxs-lookup"><span data-stu-id="52757-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="52757-108">Si no establece esta propiedad, se utilizará el nivel de autenticación COM predeterminado para el sistema.</span><span class="sxs-lookup"><span data-stu-id="52757-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="52757-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="52757-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="52757-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="52757-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52757-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52757-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="52757-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="52757-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="52757-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52757-113">Remarks</span></span>

<span data-ttu-id="52757-114">El valor authenticationLevel permite solicitar el nivel de autenticación DCOM y la privacidad que se va a usar en una conexión.</span><span class="sxs-lookup"><span data-stu-id="52757-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="52757-115">La configuración va desde sin autenticación a autenticación cifrada por paquete.</span><span class="sxs-lookup"><span data-stu-id="52757-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="52757-116">Value</span><span class="sxs-lookup"><span data-stu-id="52757-116">Value</span></span>        | <span data-ttu-id="52757-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="52757-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52757-118">None</span><span class="sxs-lookup"><span data-stu-id="52757-118">None</span></span>         | <span data-ttu-id="52757-119">No usa ninguna autenticación.</span><span class="sxs-lookup"><span data-stu-id="52757-119">Does not use any authentication.</span></span> <span data-ttu-id="52757-120">Se omiten todas las configuraciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="52757-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="52757-121">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="52757-121">Default</span></span>      | <span data-ttu-id="52757-122">Usa una negociación de seguridad estándar para seleccionar un nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="52757-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="52757-123">Esta es la configuración recomendada porque el cliente implicado en la transacción se negociará con el nivel de autenticación especificado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="52757-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="52757-124">DCOM no seleccionará el valor ninguno durante una sesión de negociación.</span><span class="sxs-lookup"><span data-stu-id="52757-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="52757-125">Conectar</span><span class="sxs-lookup"><span data-stu-id="52757-125">Connect</span></span>      | <span data-ttu-id="52757-126">Autentica las credenciales del cliente solo cuando el cliente intenta conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="52757-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="52757-127">Una vez realizada una conexión, no se realiza ninguna comprobación de autenticación adicional.</span><span class="sxs-lookup"><span data-stu-id="52757-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="52757-128">Call</span><span class="sxs-lookup"><span data-stu-id="52757-128">Call</span></span>         | <span data-ttu-id="52757-129">Autentica las credenciales del cliente solo al principio de cada llamada, cuando el servidor recibe la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52757-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="52757-130">Los encabezados de paquete están firmados, pero los paquetes de datos intercambiados entre el cliente y el servidor no están firmados ni cifrados.</span><span class="sxs-lookup"><span data-stu-id="52757-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="52757-131">PKT</span><span class="sxs-lookup"><span data-stu-id="52757-131">Pkt</span></span>          | <span data-ttu-id="52757-132">Autentica que todos los paquetes de datos se reciben del cliente esperado.</span><span class="sxs-lookup"><span data-stu-id="52757-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="52757-133">Similar a Call; Los encabezados de paquete están firmados pero no cifrados.</span><span class="sxs-lookup"><span data-stu-id="52757-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="52757-134">Los paquetes no están firmados ni cifrados.</span><span class="sxs-lookup"><span data-stu-id="52757-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="52757-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="52757-135">PktIntegrity</span></span> | <span data-ttu-id="52757-136">Autentica y comprueba que no se ha modificado ninguno de los paquetes de datos transferidos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="52757-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="52757-137">Cada paquete de datos está firmado, asegurándose de que los paquetes no se han modificado durante el tránsito.</span><span class="sxs-lookup"><span data-stu-id="52757-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="52757-138">Ninguno de los paquetes de datos está cifrado.</span><span class="sxs-lookup"><span data-stu-id="52757-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="52757-139">PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="52757-139">PktPrivacy</span></span>   | <span data-ttu-id="52757-140">Autentica todos los niveles de suplantación anteriores y firma y cifra cada paquete de datos.</span><span class="sxs-lookup"><span data-stu-id="52757-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="52757-141">Esto garantiza que toda la comunicación entre el cliente y el servidor es confidencial.</span><span class="sxs-lookup"><span data-stu-id="52757-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="52757-142">Puede establecer el nivel de autenticación de los objetos [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)y [**SwbemLocator**](swbemlocator.md) estableciendo la propiedad **AuthenticationLevel** en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="52757-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="52757-143">En el ejemplo siguiente se muestra cómo establecer el nivel de autenticación para un objeto **SwbemObject** .</span><span class="sxs-lookup"><span data-stu-id="52757-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="52757-144">También puede especificar los niveles de autenticación como parte de un moniker.</span><span class="sxs-lookup"><span data-stu-id="52757-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="52757-145">En el ejemplo siguiente se establece el nivel de autenticación y el nivel de suplantación, y se recupera una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="52757-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="52757-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52757-146">Requirements</span></span>



| <span data-ttu-id="52757-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52757-147">Requirement</span></span> | <span data-ttu-id="52757-148">Value</span><span class="sxs-lookup"><span data-stu-id="52757-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52757-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52757-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52757-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52757-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52757-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52757-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52757-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52757-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52757-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52757-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="52757-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52757-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52757-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52757-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52757-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52757-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="52757-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="52757-157">CLSID</span></span><br/>                    | <span data-ttu-id="52757-158">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="52757-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="52757-159">IID</span><span class="sxs-lookup"><span data-stu-id="52757-159">IID</span></span><br/>                      | <span data-ttu-id="52757-160">\_ISWBEMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="52757-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="52757-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="52757-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52757-162">Establecer la \_ seguridad del proceso de la aplicación cliente \_</span><span class="sxs-lookup"><span data-stu-id="52757-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="52757-163">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="52757-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="52757-164">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="52757-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

