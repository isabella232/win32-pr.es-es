---
title: Función DsBackupRead (Ntdsbcli. h)
description: Lee un bloque de datos del archivo abierto actual, en un búfer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupRead
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996297"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="73bf7-104">DsBackupRead función)</span><span class="sxs-lookup"><span data-stu-id="73bf7-104">DsBackupRead function</span></span>

<span data-ttu-id="73bf7-105">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="73bf7-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="73bf7-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="73bf7-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="73bf7-107">A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="73bf7-108">La función **DsBackupRead** Lee un bloque de datos del archivo abierto actual, en un búfer.</span><span class="sxs-lookup"><span data-stu-id="73bf7-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="73bf7-109">Se espera que la aplicación cliente llame a esta función repetidamente hasta que se haya recibido todo el archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73bf7-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="73bf7-110">La función [**DsBackupOpenFile**](dsbackupopenfile.md) proporciona el tamaño completo del archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73bf7-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="73bf7-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73bf7-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="73bf7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73bf7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73bf7-113">*HBC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-114">Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="73bf7-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="73bf7-115">*pvBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-116">Puntero a un búfer que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="73bf7-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="73bf7-117">Este búfer debe tener un tamaño mínimo de *cbBuffer* bytes.</span><span class="sxs-lookup"><span data-stu-id="73bf7-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="73bf7-118">*cbBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-119">Contiene el tamaño, en bytes, del búfer en *pvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="73bf7-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="73bf7-120">Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.</span><span class="sxs-lookup"><span data-stu-id="73bf7-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="73bf7-121">*pcbRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-122">Puntero a un valor **DWORD** que recibe el número real de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="73bf7-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="73bf7-123">Puede ser menor que el número de bytes solicitados porque algunos transportes fragmentan el búfer que se está transmitiendo en lugar de llenar todo el búfer con datos.</span><span class="sxs-lookup"><span data-stu-id="73bf7-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73bf7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73bf7-124">Return value</span></span>

<span data-ttu-id="73bf7-125">Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="73bf7-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="73bf7-126">Entre los posibles códigos de error se incluyen los siguientes.</span><span class="sxs-lookup"><span data-stu-id="73bf7-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="73bf7-127">**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="73bf7-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-128">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="73bf7-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="73bf7-129">**ERROR de \_ control de \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="73bf7-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-130">Se alcanzó el final del archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="73bf7-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73bf7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73bf7-131">Requirements</span></span>



| <span data-ttu-id="73bf7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="73bf7-132">Requirement</span></span> | <span data-ttu-id="73bf7-133">Value</span><span class="sxs-lookup"><span data-stu-id="73bf7-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73bf7-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73bf7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="73bf7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73bf7-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73bf7-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73bf7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="73bf7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73bf7-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73bf7-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73bf7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="73bf7-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="73bf7-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73bf7-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="73bf7-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="73bf7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73bf7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73bf7-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73bf7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="73bf7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bf7-145">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="73bf7-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="73bf7-146">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="73bf7-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="73bf7-147">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="73bf7-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="73bf7-148">Copia de seguridad de un servidor Active Directory</span><span class="sxs-lookup"><span data-stu-id="73bf7-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="73bf7-149">Funciones de copia de seguridad de directorios</span><span class="sxs-lookup"><span data-stu-id="73bf7-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 

