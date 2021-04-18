---
title: Objeto ConnectionOptions (WSManDisp. h)
description: El objeto ConnectionOptions se pasa al método CreateSession para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Objeto ConnectionOptions Administración remota de Windows
- Administración remota de Windows de objeto ConnectionOptions, descrito
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705157"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="771ef-105">Objeto ConnectionOptions</span><span class="sxs-lookup"><span data-stu-id="771ef-105">ConnectionOptions object</span></span>

<span data-ttu-id="771ef-106">El objeto **ConnectionOptions** se pasa al método [**createSession**](wsman-createsession.md) para proporcionar el nombre de usuario y la contraseña asociados a la cuenta local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="771ef-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="771ef-107">Si no se proporciona ningún parámetro, las credenciales de la cuenta que ejecuta el script se establecen en los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="771ef-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="771ef-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="771ef-108">Members</span></span>

<span data-ttu-id="771ef-109">El objeto **ConnectionOptions** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="771ef-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="771ef-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="771ef-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="771ef-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="771ef-111">Properties</span></span>

<span data-ttu-id="771ef-112">El objeto **ConnectionOptions** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="771ef-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="771ef-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="771ef-113">Property</span></span>                                                  | <span data-ttu-id="771ef-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="771ef-114">Access type</span></span>           | <span data-ttu-id="771ef-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="771ef-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="771ef-116">**Contraseña**</span><span class="sxs-lookup"><span data-stu-id="771ef-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="771ef-117">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="771ef-117">Write-only</span></span><br/> | <span data-ttu-id="771ef-118">Establece la contraseña de una cuenta local o de dominio en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="771ef-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="771ef-119">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="771ef-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="771ef-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="771ef-120">Read/write</span></span><br/> | <span data-ttu-id="771ef-121">Establece y obtiene el nombre de usuario de una cuenta local o de dominio en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="771ef-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="771ef-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="771ef-122">Remarks</span></span>

<span data-ttu-id="771ef-123">El objeto **ConnectionOptions** corresponde a la interfaz [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="771ef-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="771ef-124">Si una aplicación cliente de Administración remota de Windows se ejecuta bajo suplantación, se produce un error si se establece la propiedad [**contraseña**](connectionoptions-password.md) .</span><span class="sxs-lookup"><span data-stu-id="771ef-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="771ef-125">Una aplicación cliente es un script u otro programa que envía una solicitud a WinRM en el equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="771ef-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="771ef-126">Es posible que la aplicación cliente se esté ejecutando bajo suplantación porque llamó a una función como [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="771ef-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="771ef-127">Una página Active Server (ASP) o un servicio no pueden solicitar un nombre de usuario y una contraseña si el proceso de ASP se ejecuta en una cuenta que suplanta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="771ef-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="771ef-128">La marca **WSManFlagCredUserNamePassword** debe establecerse en la llamada [**WSman. createSession**](wsman-createsession.md) cuando se usa el [**nombre de usuario**](connectionoptions-username.md) y la [**contraseña**](connectionoptions-password.md) para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="771ef-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="771ef-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="771ef-129">Examples</span></span>

<span data-ttu-id="771ef-130">En el ejemplo de código de VBScript siguiente se muestra cómo crear un objeto **ConnectionOptions** , cómo establecer las propiedades de la cuenta en el equipo remoto y cómo usarla para crear un objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="771ef-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="771ef-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="771ef-131">Requirements</span></span>



| <span data-ttu-id="771ef-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="771ef-132">Requirement</span></span> | <span data-ttu-id="771ef-133">Value</span><span class="sxs-lookup"><span data-stu-id="771ef-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="771ef-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771ef-134">Minimum supported client</span></span><br/> | <span data-ttu-id="771ef-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="771ef-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="771ef-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771ef-136">Minimum supported server</span></span><br/> | <span data-ttu-id="771ef-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="771ef-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="771ef-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="771ef-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="771ef-139"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="771ef-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="771ef-140">IDL</span><span class="sxs-lookup"><span data-stu-id="771ef-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="771ef-141"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="771ef-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="771ef-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="771ef-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="771ef-143"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="771ef-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="771ef-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="771ef-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771ef-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771ef-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="771ef-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="771ef-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771ef-147">Autenticación para conexiones remotas</span><span class="sxs-lookup"><span data-stu-id="771ef-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="771ef-148">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="771ef-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="771ef-149">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="771ef-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="771ef-150">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="771ef-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="771ef-151">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="771ef-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="771ef-152">Obtención de datos del equipo local</span><span class="sxs-lookup"><span data-stu-id="771ef-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="771ef-153">Obtención de datos de un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="771ef-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

