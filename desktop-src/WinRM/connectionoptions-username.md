---
title: Propiedad ConnectionOptions. UserName (WSManDisp. h)
description: Establece y obtiene el nombre de usuario de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina el nombre de usuario para la autenticación.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Propiedad UserName Administración remota de Windows
- Propiedad UserName Administración remota de Windows, objeto ConnectionOptions
- Administración remota de Windows de objeto ConnectionOptions, propiedad UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150587"
---
# <a name="connectionoptionsusername-property"></a><span data-ttu-id="c7247-107">Propiedad ConnectionOptions. UserName</span><span class="sxs-lookup"><span data-stu-id="c7247-107">ConnectionOptions.UserName property</span></span>

<span data-ttu-id="c7247-108">Establece y obtiene el nombre de usuario de una cuenta de dominio o local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c7247-108">Sets and gets the user name of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="c7247-109">Esta propiedad determina el nombre de usuario para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c7247-109">This property determines the user name for authentication.</span></span> <span data-ttu-id="c7247-110">Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="c7247-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="c7247-111">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c7247-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7247-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7247-112">Syntax</span></span>


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a><span data-ttu-id="c7247-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c7247-113">Property value</span></span>

<span data-ttu-id="c7247-114">Cadena que contiene el nombre de usuario de una cuenta de dominio o local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c7247-114">String that contains the user name of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="c7247-115">Si no se proporciona ningún valor y no se establece la marca **WSManFlagCredUsernamePassword** , se usa el nombre de usuario de la cuenta que ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="c7247-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the user name of the account that is running the script is used.</span></span>

<span data-ttu-id="c7247-116">Si no se proporciona ningún valor y se establece la marca **WSManFlagCredUsernamePassword** , el script le pedirá al usuario que escriba el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="c7247-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the user name and password.</span></span> <span data-ttu-id="c7247-117">Si no se especifica un nombre de usuario y una contraseña válidos, se devuelve un error de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c7247-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7247-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7247-118">Remarks</span></span>

<span data-ttu-id="c7247-119">La siguiente sintaxis se usa para especificar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c7247-119">The following syntax is used to specify this property.</span></span>


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



<span data-ttu-id="c7247-120">Puede proporcionar el **nombre de usuario** y la [**contraseña**](connectionoptions-password.md) de una cuenta de dominio al usar la autenticación [*Negotiate*](windows-remote-management-glossary.md) o *Kerberos* , o para una cuenta local con autenticación [*básica*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="c7247-120">You can supply **UserName** and [**Password**](connectionoptions-password.md) for a domain account when using [*negotiate*](windows-remote-management-glossary.md) or *Kerberos* authentication, or for a local account with [*Basic*](windows-remote-management-glossary.md) authentication.</span></span> <span data-ttu-id="c7247-121">Para conectarse a una cuenta local, los marcadores [**WSMan. createSession**](wsman-createsession.md) deben contener la combinación de la marca **WSManFlagUseBasic** y la marca **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="c7247-121">To connect to a local account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseBasic** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="c7247-122">Para conectarse a una cuenta de dominio, las marcas **WSMan. createSession** deben contener la combinación de la marca **WSManFlagUseNegotiate** y la marca **WsmanFlagCredUserNamePassword** , o la combinación de la marca **WSManFlagUseKerberos** y la marca **WsmanFlagCredUserNamePassword** .</span><span class="sxs-lookup"><span data-stu-id="c7247-122">To connect to a domain account, the **WSMan.CreateSession** flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag, or the combination of the **WSManFlagUseKerberos** flag and the **WsmanFlagCredUserNamePassword** flag.</span></span> <span data-ttu-id="c7247-123">En el caso de una cuenta de dominio, el **nombre de usuario** debe especificarse con el formato "nombre de usuario de equipo \\ ", donde la parte "equipo" de la cadena puede ser el nombre o la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="c7247-123">For a domain account, **UserName** must be specified in the form "computer\\username", where the "computer" part of the string can be either the name or the IP address.</span></span> <span data-ttu-id="c7247-124">Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="c7247-124">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



<span data-ttu-id="c7247-125">Para conectarse a una cuenta de dominio, las marcas [**WSMan. createSession**](wsman-createsession.md) deben contener la combinación de la marca **WSManFlagUseNegotiate** y la marca **WsmanFlagCredUserNamePassword** para conectarse a una cuenta de dominio, lo que requiere la autenticación Negotiate.</span><span class="sxs-lookup"><span data-stu-id="c7247-125">For connecting to a domain account, the [**WSMan.CreateSession**](wsman-createsession.md) flags must contain the combination of the **WSManFlagUseNegotiate** flag and the **WsmanFlagCredUserNamePassword** flag for connecting to a domain account, which requires Negotiate authentication.</span></span>


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



## <a name="requirements"></a><span data-ttu-id="c7247-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7247-126">Requirements</span></span>



| <span data-ttu-id="c7247-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7247-127">Requirement</span></span> | <span data-ttu-id="c7247-128">Value</span><span class="sxs-lookup"><span data-stu-id="c7247-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7247-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7247-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c7247-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7247-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7247-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7247-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c7247-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7247-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7247-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7247-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7247-134"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7247-134"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7247-135">IDL</span><span class="sxs-lookup"><span data-stu-id="c7247-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7247-136"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7247-136"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7247-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7247-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7247-138"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7247-138"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7247-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7247-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7247-140"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7247-140"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7247-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7247-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7247-142">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="c7247-142">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





