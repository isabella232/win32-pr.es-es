---
title: Función DsIsNTDSOnline (Ntdsbcli. h)
description: Determina si Active Directory Domain Services están en línea en el servidor especificado.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150325"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="6900b-104">DsIsNTDSOnline función)</span><span class="sxs-lookup"><span data-stu-id="6900b-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="6900b-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6900b-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6900b-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6900b-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6900b-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="6900b-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="6900b-108">La función **DsIsNTDSOnline** determina si Active Directory Domain Services están en línea en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="6900b-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6900b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6900b-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="6900b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6900b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6900b-111">*szServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6900b-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6900b-112">Puntero a una cadena terminada en null que contiene el nombre del servidor que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="6900b-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="6900b-113">Las barras diagonales inversas anteriores son opcionales.</span><span class="sxs-lookup"><span data-stu-id="6900b-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="6900b-114">El servidor debe ser el mismo equipo desde el que se llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="6900b-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="6900b-115">El nombre del servidor no puede contener caracteres de subrayado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="6900b-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="6900b-116">Un ejemplo de un nombre de servidor es " \\ \\ server1".</span><span class="sxs-lookup"><span data-stu-id="6900b-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="6900b-117">*pfNTDSOnline* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6900b-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6900b-118">Puntero al valor **bool** que recibe el resultado.</span><span class="sxs-lookup"><span data-stu-id="6900b-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="6900b-119">Recibe **true** si el servicio de directorio está en línea o **false** si el servicio de directorio está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6900b-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6900b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6900b-120">Return value</span></span>

<span data-ttu-id="6900b-121">Devuelve **S \_ OK** si la función es correcta o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6900b-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="6900b-122">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6900b-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="6900b-123">**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="6900b-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="6900b-124">El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="6900b-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="6900b-125">La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="6900b-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="6900b-126">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="6900b-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="6900b-127">No se encuentra el servidor en *szServerName* , no es un controlador de dominio o *szServerName* no tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="6900b-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="6900b-128">Este valor se define en Ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="6900b-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="6900b-129">**enlace de RPC \_ S \_ no válido \_**</span><span class="sxs-lookup"><span data-stu-id="6900b-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="6900b-130">Se está llamando a la función [**DsIsNTDSOnline**](dsisntdsonline.md) de forma remota o el servidor de *szServerName* no es un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="6900b-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6900b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6900b-131">Remarks</span></span>

<span data-ttu-id="6900b-132">Llame a esta función antes de llamar a cualquiera de las funciones de copia de seguridad o restauración de directorios.</span><span class="sxs-lookup"><span data-stu-id="6900b-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="6900b-133">El directorio debe estar en línea para realizar una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6900b-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="6900b-134">El directorio debe estar sin conexión para realizar una restauración.</span><span class="sxs-lookup"><span data-stu-id="6900b-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="6900b-135">Solo se puede llamar a esta función desde un controlador de dominio que también sea el servidor de destino especificado en *szServerName*.</span><span class="sxs-lookup"><span data-stu-id="6900b-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="6900b-136">No se puede llamar a esta función de forma remota.</span><span class="sxs-lookup"><span data-stu-id="6900b-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="6900b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6900b-137">Requirements</span></span>



| <span data-ttu-id="6900b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6900b-138">Requirement</span></span> | <span data-ttu-id="6900b-139">Value</span><span class="sxs-lookup"><span data-stu-id="6900b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6900b-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6900b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6900b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6900b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6900b-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6900b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6900b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6900b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6900b-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6900b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6900b-145"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="6900b-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="6900b-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6900b-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="6900b-147"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6900b-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="6900b-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6900b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6900b-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6900b-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="6900b-150">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6900b-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6900b-151">**DsIsNTDSOnlineW** (Unicode) y **DsIsNTDSOnlineA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6900b-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6900b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6900b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6900b-153">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="6900b-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="6900b-154">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="6900b-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="6900b-155">Copia de seguridad y restauración de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="6900b-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 

