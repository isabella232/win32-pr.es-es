---
title: Función DsSetAuthIdentity (Ntdsbcli. h)
description: Establece el contexto de seguridad en el que se llama a las API de copia de seguridad de directorio.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491236"
---
# <a name="dssetauthidentity-function"></a><span data-ttu-id="97177-104">DsSetAuthIdentity función)</span><span class="sxs-lookup"><span data-stu-id="97177-104">DsSetAuthIdentity function</span></span>

<span data-ttu-id="97177-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="97177-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97177-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="97177-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="97177-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="97177-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="97177-108">La función **DsSetAuthIdentity** establece el contexto de seguridad en el que se llama a las API de copia de seguridad de directorio.</span><span class="sxs-lookup"><span data-stu-id="97177-108">The **DsSetAuthIdentity** function sets the security context under which the directory backup APIs are called.</span></span>

## <a name="syntax"></a><span data-ttu-id="97177-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97177-109">Syntax</span></span>


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a><span data-ttu-id="97177-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97177-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97177-111">*szUserName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97177-111">*szUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97177-112">Cadena terminada en null que especifica el nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="97177-112">The null-terminated string that specifies the user name.</span></span>

</dd> <dt>

<span data-ttu-id="97177-113">*szDomainName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97177-113">*szDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97177-114">Cadena terminada en null que especifica el nombre del dominio al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="97177-114">The null-terminated string that specifies the name of the domain that the user belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="97177-115">*szPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97177-115">*szPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97177-116">Cadena terminada en null que especifica la contraseña del usuario en el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="97177-116">The null-terminated string that specifies the password of the user in the specified domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97177-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97177-117">Return value</span></span>

<span data-ttu-id="97177-118">Si se realiza correctamente, devuelve un código de error **HRESULT** estándar; de lo contrario, se devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="97177-118">If successful, returns a standard **HRESULT** success codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="97177-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97177-119">Remarks</span></span>

<span data-ttu-id="97177-120">Si no se llama a **DsSetAuthIdentity** , se supone el contexto de seguridad del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="97177-120">If **DsSetAuthIdentity** is not called, security context of the current process is assumed.</span></span>

## <a name="requirements"></a><span data-ttu-id="97177-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97177-121">Requirements</span></span>



| <span data-ttu-id="97177-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97177-122">Requirement</span></span> | <span data-ttu-id="97177-123">Value</span><span class="sxs-lookup"><span data-stu-id="97177-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97177-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97177-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97177-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97177-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97177-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97177-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97177-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97177-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97177-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97177-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97177-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="97177-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="97177-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97177-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="97177-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97177-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="97177-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97177-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97177-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97177-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="97177-134">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="97177-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="97177-135">**DsSetAuthIdentityW** (Unicode) y **DsSetAuthIdentityA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="97177-135">**DsSetAuthIdentityW** (Unicode) and **DsSetAuthIdentityA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="97177-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="97177-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97177-137">Copia de seguridad y restauración de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="97177-137">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="97177-138">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="97177-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

