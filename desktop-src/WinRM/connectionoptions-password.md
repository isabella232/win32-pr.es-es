---
title: Propiedad ConnectionOptions. Password (WSManDisp. h)
description: Establece la contraseña de una cuenta de dominio o local en el equipo remoto. Esta propiedad determina la contraseña para la autenticación.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Propiedad password Administración remota de Windows
- Propiedad password Administración remota de Windows, objeto ConnectionOptions
- Administración remota de Windows de objeto ConnectionOptions, propiedad Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150588"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="689de-107">ConnectionOptions. Password (propiedad)</span><span class="sxs-lookup"><span data-stu-id="689de-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="689de-108">Establece la contraseña de una cuenta de dominio o local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="689de-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="689de-109">Esta propiedad determina la contraseña para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="689de-109">This property determines the password for authentication.</span></span> <span data-ttu-id="689de-110">Para obtener más información, consulte [autenticación para conexiones remotas](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="689de-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="689de-111">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="689de-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="689de-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="689de-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="689de-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="689de-113">Property value</span></span>

<span data-ttu-id="689de-114">Cadena que contiene la contraseña de una cuenta de dominio o local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="689de-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="689de-115">Si no se proporciona ningún valor y no se establece la marca **WSManFlagCredUsernamePassword** , se usa la contraseña de la cuenta que ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="689de-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="689de-116">Si no se proporciona ningún valor y se establece la marca **WSManFlagCredUsernamePassword** , el script le pedirá al usuario que escriba la contraseña (y el nombre de usuario, si no se proporciona).</span><span class="sxs-lookup"><span data-stu-id="689de-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="689de-117">Si no se especifica un nombre de usuario y una contraseña válidos, se devuelve un error de acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="689de-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="689de-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="689de-118">Remarks</span></span>

<span data-ttu-id="689de-119">Tenga en cuenta que no puede recuperar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="689de-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="689de-120">La contraseña solo se puede establecer con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="689de-120">The password can only be set with this property.</span></span>

<span data-ttu-id="689de-121">Si crea un objeto [**ConnectionOptions**](connectionoptions.md) y usa un nombre de usuario y una contraseña para conectarse a administración remota de Windows, se debe establecer la marca **WSManFlagCredUserNamePassword** en la llamada a [**WSMan. createSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="689de-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="689de-122">Para obtener más información sobre la configuración de contraseñas, vea la sección Comentarios en [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="689de-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="689de-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="689de-123">Examples</span></span>

<span data-ttu-id="689de-124">En el ejemplo de código siguiente se crea un objeto [**ConnectionOptions**](connectionoptions.md) y se establece la **contraseña**.</span><span class="sxs-lookup"><span data-stu-id="689de-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="689de-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="689de-125">Requirements</span></span>



| <span data-ttu-id="689de-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="689de-126">Requirement</span></span> | <span data-ttu-id="689de-127">Value</span><span class="sxs-lookup"><span data-stu-id="689de-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="689de-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="689de-128">Minimum supported client</span></span><br/> | <span data-ttu-id="689de-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="689de-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="689de-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="689de-130">Minimum supported server</span></span><br/> | <span data-ttu-id="689de-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="689de-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="689de-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="689de-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="689de-133"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="689de-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="689de-134">IDL</span><span class="sxs-lookup"><span data-stu-id="689de-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="689de-135"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="689de-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="689de-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="689de-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="689de-137"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="689de-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="689de-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="689de-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="689de-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="689de-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="689de-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="689de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689de-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="689de-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





