---
description: Elimina la credencial de usuario usada para la identidad conectada.
ms.assetid: EB32832D-9A8C-4CEB-897A-7E9D24FF84DD
title: Función DeleteConnectedIdentity (Indentitystore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteConnectedIdentity
api_type:
- HeaderDef
api_location:
- Indentitystore.h
ms.openlocfilehash: 8079985f916e996a56b4203ad6ad065c1b7664e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082000"
---
# <a name="deleteconnectedidentity-function"></a><span data-ttu-id="f3aa2-103">DeleteConnectedIdentity función)</span><span class="sxs-lookup"><span data-stu-id="f3aa2-103">DeleteConnectedIdentity function</span></span>

<span data-ttu-id="f3aa2-104">Elimina la credencial de usuario usada para la identidad conectada.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-104">Deletes the user credential used for the connected identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3aa2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3aa2-105">Syntax</span></span>


```C++
SEC_ENTRY DeleteConnectedIdentity(
  _In_     PVOID  ProviderHandle,
  _In_opt_ HANDLE UserToken,
  _In_     PSID   UserSid,
  _In_     PWSTR  IdentityUserName
);
```



## <a name="parameters"></a><span data-ttu-id="f3aa2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3aa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3aa2-107">*ProviderHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3aa2-108">Identificador del proveedor de identidades.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="f3aa2-109">*UserToken* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-109">*UserToken* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3aa2-110">Token del usuario conectado cuya cuenta se va a convertir en una cuenta local.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-110">Token of the connected user whose account is going to be converted to a local account.</span></span> <span data-ttu-id="f3aa2-111">Si *UserToken* no es **null**, el proveedor de identidades usa este token para cargar el perfil de usuario y limpiar los Estados conectados.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-111">If *UserToken* is not **NULL**, the identity provider uses this token to load the user profile and clean up connected states.</span></span> <span data-ttu-id="f3aa2-112">Si *UserToken* es **null**, LSA está forzando la desconexión.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-112">If *UserToken* is **NULL**, LSA is forcing the disconnection.</span></span> <span data-ttu-id="f3aa2-113">El proveedor de identidades debe limpiar todos los Estados conectados globales de este usuario, pero el proveedor no tiene que limpiar los Estados conectados en el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-113">The identity provider should clean up any global connected states on this user, but the provider does not have to clean up connected states in the user profile.</span></span>

</dd> <dt>

<span data-ttu-id="f3aa2-114">*UserSid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-114">*UserSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3aa2-115">SID principal del usuario conectado.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-115">The primary SID of the connected user.</span></span> <span data-ttu-id="f3aa2-116">Si *UserToken* no es **null**, este parámetro es el SID de usuario del token.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-116">If *UserToken* is not **NULL**, this parameter is the user SID of the token.</span></span> <span data-ttu-id="f3aa2-117">Si *UserToken* es **null**, este parámetro se utiliza para identificar al usuario conectado y limpiar los Estados conectados globales de dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-117">If *UserToken* is **NULL**, this parameter is used to identify the connected user and clean up global connected states of that user.</span></span>

</dd> <dt>

<span data-ttu-id="f3aa2-118">*IdentityUserName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-118">*IdentityUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3aa2-119">El nombre de usuario de la identidad.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-119">The user name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3aa2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3aa2-120">Return value</span></span>

<span data-ttu-id="f3aa2-121">Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-121">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="f3aa2-122">Si se produce un error en la función, la función puede devolver uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-122">If the function fails, the function may return one of the following error codes.</span></span>



| <span data-ttu-id="f3aa2-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3aa2-123">Return value</span></span>                                                                                               | <span data-ttu-id="f3aa2-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3aa2-124">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3aa2-125"><dt>ESTADO \_ parámetro no válido \_</dt></span><span class="sxs-lookup"><span data-stu-id="f3aa2-125"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>      | <span data-ttu-id="f3aa2-126">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-126">A parameter is not valid.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="f3aa2-127"><dt>ESTADO \_ no \_ tal \_ usuario</dt></span><span class="sxs-lookup"><span data-stu-id="f3aa2-127"><dt>STATUS\_NO\_SUCH\_USER</dt></span></span> </dl>          | <span data-ttu-id="f3aa2-128">El usuario identificado por *UserSid* no existe, no está conectado actualmente o no hay ninguna identidad cuyo nombre de usuario coincida con *IdentityUserName*.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-128">The user identified by *UserSid* does not exist, is not currently connected, or there is no identity whose user name matches *IdentityUserName*.</span></span><br/> |
| <dl> <span data-ttu-id="f3aa2-129"><dt>Estado de \_ recursos insuficientes \_</dt></span><span class="sxs-lookup"><span data-stu-id="f3aa2-129"><dt>STATUS\_INSUFFICIENT\_RESOURCES</dt></span></span> </dl> | <span data-ttu-id="f3aa2-130">No hay suficiente memoria para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3aa2-130">There is not enough memory to process the request.</span></span><br/>                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="f3aa2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3aa2-131">Requirements</span></span>



| <span data-ttu-id="f3aa2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3aa2-132">Requirement</span></span> | <span data-ttu-id="f3aa2-133">Value</span><span class="sxs-lookup"><span data-stu-id="f3aa2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3aa2-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3aa2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f3aa2-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f3aa2-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3aa2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f3aa2-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3aa2-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3aa2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3aa2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3aa2-139"><dt>Indentitystore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3aa2-139"><dt>Indentitystore.h</dt></span></span> </dl> |



 

 




