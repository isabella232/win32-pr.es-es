---
title: Función DsSetCurrentBackupLog (Ntdsbcli. h)
description: Establece el número de registro de copia de seguridad actual después de una restauración correcta.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905372"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="b6b31-104">DsSetCurrentBackupLog función)</span><span class="sxs-lookup"><span data-stu-id="b6b31-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="b6b31-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6b31-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6b31-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b6b31-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b6b31-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="b6b31-108">La función **DsSetCurrentBackupLog** establece el número de registro de copia de seguridad actual después de una restauración correcta.</span><span class="sxs-lookup"><span data-stu-id="b6b31-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="b6b31-109">Dado que Active Directory Domain Services solo admiten el registro circular, esta función no se utiliza normalmente.</span><span class="sxs-lookup"><span data-stu-id="b6b31-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b31-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6b31-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="b6b31-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6b31-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b31-112">*szServerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-113">Puntero a una cadena terminada en null que contiene el nombre del servidor para el que se va a establecer el número de registro de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6b31-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="b6b31-114">Las barras diagonales inversas anteriores son opcionales.</span><span class="sxs-lookup"><span data-stu-id="b6b31-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="b6b31-115">El servidor debe ser el mismo equipo desde el que se llama a esta función.</span><span class="sxs-lookup"><span data-stu-id="b6b31-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="b6b31-116">El nombre del servidor no puede contener caracteres de subrayado ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="b6b31-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="b6b31-117">Un ejemplo de un nombre de servidor es " \\ \\ server1".</span><span class="sxs-lookup"><span data-stu-id="b6b31-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="b6b31-118">*dwCurrentLog* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6b31-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-119">Contiene el número de registro de copia de seguridad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b6b31-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b31-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6b31-120">Return value</span></span>

<span data-ttu-id="b6b31-121">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b6b31-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="b6b31-122">En la lista siguiente se enumeran los posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="b6b31-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="b6b31-123">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="b6b31-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-124">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b6b31-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b6b31-125">**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="b6b31-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="b6b31-126">Error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="b6b31-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6b31-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6b31-127">Remarks</span></span>

<span data-ttu-id="b6b31-128">Normalmente no es necesario llamar a la función **DsSetCurrentBackupLog** .</span><span class="sxs-lookup"><span data-stu-id="b6b31-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="b6b31-129">Las funciones de copia de seguridad determinan y establecen automáticamente el último número de registro del que se realizó una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b6b31-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="b6b31-130">Use **DsSetCurrentBackupLog** para impedir que otra copia de seguridad incremental se realice correctamente hasta que se realice una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="b6b31-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b31-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b31-131">Requirements</span></span>



| <span data-ttu-id="b6b31-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b31-132">Requirement</span></span> | <span data-ttu-id="b6b31-133">Value</span><span class="sxs-lookup"><span data-stu-id="b6b31-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b31-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6b31-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b31-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6b31-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6b31-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6b31-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b31-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6b31-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6b31-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6b31-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b31-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b31-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6b31-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6b31-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6b31-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b31-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6b31-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6b31-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b31-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b31-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6b31-144">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b6b31-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6b31-145">**DsSetCurrentBackupLogW** (Unicode) y **DsSetCurrentBackupLogA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6b31-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="b6b31-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6b31-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b31-147">Copia de seguridad y restauración de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="b6b31-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="b6b31-148">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="b6b31-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

