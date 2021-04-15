---
title: Método WSMan. CreateSession (WSManDisp. h)
description: Crea un objeto de sesión que se puede usar para las operaciones de red subsiguientes.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Método CreateSession Administración remota de Windows
- Administración remota de Windows método CreateSession, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534528"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="9c556-106">WSMan. CreateSession (método)</span><span class="sxs-lookup"><span data-stu-id="9c556-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="9c556-107">Crea un objeto de [**sesión**](session.md) que se puede usar para las operaciones de red subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="9c556-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c556-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c556-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9c556-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c556-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c556-110">*conexión* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c556-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c556-111">Protocolo y servicio al que se va a conectar, incluido IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="9c556-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="9c556-112">El formato de la información de conexión es el siguiente: <sufijo de dirección de *transporte* ><  >< >.</span><span class="sxs-lookup"><span data-stu-id="9c556-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="9c556-113">Para obtener ejemplos, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9c556-113">For examples, see Remarks.</span></span> <span data-ttu-id="9c556-114">Si no se proporciona información de conexión, se utiliza el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9c556-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="9c556-115">*marcas* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c556-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c556-116">Marcas de sesión que especifican el método de autenticación, como [*negociar autenticación*](windows-remote-management-glossary.md) o [*autenticación implícita*](windows-remote-management-glossary.md), para conectarse a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="9c556-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="9c556-117">Estas marcas también especifican otra información de conexión de la sesión, como la codificación o el cifrado.</span><span class="sxs-lookup"><span data-stu-id="9c556-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="9c556-118">Este parámetro debe contener una o varias marcas en **\_ \_ WSManSessionFlags** para una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="9c556-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="9c556-119">Para obtener más información, vea [constantes de sesión](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9c556-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="9c556-120">No se requiere ninguna configuración de marca para una conexión a WinRM en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9c556-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="9c556-121">El valor predeterminado es **WSManFlagUseNegotiate**.</span><span class="sxs-lookup"><span data-stu-id="9c556-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="9c556-122">Para obtener más información, consulte [autenticación para las conexiones remotas](authentication-for-remote-connections.md) y el parámetro *connectionOptions* .</span><span class="sxs-lookup"><span data-stu-id="9c556-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9c556-123">*connectionOptions* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9c556-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c556-124">Un puntero a un objeto [**ConnectionOptions**](connectionoptions.md) que contiene un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="9c556-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="9c556-125">El valor predeterminado es **null**.</span><span class="sxs-lookup"><span data-stu-id="9c556-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c556-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c556-126">Return value</span></span>

<span data-ttu-id="9c556-127">Objeto de [**sesión**](session.md) que se puede usar para realizar operaciones WinRM locales o remotas.</span><span class="sxs-lookup"><span data-stu-id="9c556-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c556-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c556-128">Remarks</span></span>

<span data-ttu-id="9c556-129">El método **createSession** inicializa el objeto de [**sesión**](session.md) mediante la recopilación de parámetros, como marcas, credenciales y una cadena de conexión para el parámetro de *conexión* .</span><span class="sxs-lookup"><span data-stu-id="9c556-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="9c556-130">**CreateSession** realmente no se conecta al equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="9c556-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="9c556-131">Si no se puede establecer la conexión, se produce un error en la primera operación de **sesión** , como [**Get**](session-get.md) o [**Enumerate**](session-enumerate.md), después de la llamada a **createSession**.</span><span class="sxs-lookup"><span data-stu-id="9c556-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="9c556-132">Este comportamiento difiere de una conexión [*WMI*](windows-remote-management-glossary.md) a un [*espacio de nombres*](windows-remote-management-glossary.md) de un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="9c556-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="9c556-133">Para obtener más información, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="9c556-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="9c556-134">El siguiente ejemplo de código VBScript se usa para llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="9c556-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="9c556-135">En los ejemplos siguientes se muestran los distintos formatos que se usan para especificar la información de conexión en el parámetro de *conexión* (al crear una sesión https, el campo de *Dirección* <> debe coincidir con el nombre del certificado de equipo del servidor; de lo contrario, se producirá un error):</span><span class="sxs-lookup"><span data-stu-id="9c556-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="9c556-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="9c556-136">"https://service"</span></span>

    <span data-ttu-id="9c556-137">Usa HTTPS para conectarse a la ubicación del servicio Web predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9c556-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="9c556-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="9c556-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="9c556-139">Usa HTTPS para conectarse a la ubicación del servicio Web específica.</span><span class="sxs-lookup"><span data-stu-id="9c556-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="9c556-140">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="9c556-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="9c556-141">Usa HTTPS e IPv6 con el puerto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9c556-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="9c556-142">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/wsman"</span><span class="sxs-lookup"><span data-stu-id="9c556-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="9c556-143">Usa HTTPS e IPv6 con el puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="9c556-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="9c556-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c556-144">Examples</span></span>

<span data-ttu-id="9c556-145">En el ejemplo de código de VBScript siguiente se crea una sesión en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9c556-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="9c556-146">En el siguiente ejemplo de código de VBScript se crea una sesión en un equipo remoto que se identifica mediante una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="9c556-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="9c556-147">El script proporciona un nombre de usuario y una contraseña para una cuenta.</span><span class="sxs-lookup"><span data-stu-id="9c556-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="9c556-148">Las marcas **WSManFlagCredUserNamePassword** y **WSManFlagUseBasic** se combinan para indicar que la cuenta es una cuenta local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="9c556-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="9c556-149">Si se produce un error en la creación de la sesión, el script finaliza.</span><span class="sxs-lookup"><span data-stu-id="9c556-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="9c556-150">El script usa los métodos que devuelven la constante, como [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="9c556-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="9c556-151">Para ejecutar este script, tenga en cuenta que debe configurar las opciones de configuración predeterminadas para el cliente y el servidor para permitir el tráfico no cifrado y la autenticación básica (**AllowUnencrypted** establecido en **true** y Basic en **true**).</span><span class="sxs-lookup"><span data-stu-id="9c556-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="9c556-152">Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="9c556-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="9c556-153">En el siguiente ejemplo de código de VBScript, la cuenta es una cuenta de dominio y se utiliza la autenticación Negotiate.</span><span class="sxs-lookup"><span data-stu-id="9c556-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="9c556-154">Con Negotiate Authentication, debe especificar el nombre de usuario como `computername\username` o `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="9c556-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="9c556-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c556-155">Requirements</span></span>



| <span data-ttu-id="9c556-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c556-156">Requirement</span></span> | <span data-ttu-id="9c556-157">Value</span><span class="sxs-lookup"><span data-stu-id="9c556-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c556-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c556-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9c556-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c556-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9c556-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c556-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9c556-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c556-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9c556-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c556-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c556-163"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c556-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c556-164">IDL</span><span class="sxs-lookup"><span data-stu-id="9c556-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c556-165"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c556-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9c556-166">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c556-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c556-167"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c556-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c556-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c556-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c556-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c556-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c556-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c556-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c556-171">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="9c556-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="9c556-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="9c556-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="9c556-173">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="9c556-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="9c556-174">Autenticación para conexiones remotas</span><span class="sxs-lookup"><span data-stu-id="9c556-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="9c556-175">Instalación y configuración de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="9c556-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





