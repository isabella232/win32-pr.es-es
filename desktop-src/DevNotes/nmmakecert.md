---
description: Crea un certificado de usuario para su uso con conferencias de NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649933"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="68368-103">NmMakeCert función)</span><span class="sxs-lookup"><span data-stu-id="68368-103">NmMakeCert function</span></span>

<span data-ttu-id="68368-104">Crea un certificado de usuario para su uso con conferencias de NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="68368-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="68368-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68368-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="68368-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68368-107">*szFirstName*</span><span class="sxs-lookup"><span data-stu-id="68368-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-108">Nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="68368-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="68368-109">*szLastName*</span><span class="sxs-lookup"><span data-stu-id="68368-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-110">Apellidos del usuario.</span><span class="sxs-lookup"><span data-stu-id="68368-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="68368-111">*szEmailName*</span><span class="sxs-lookup"><span data-stu-id="68368-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-112">El nombre de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="68368-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="68368-113">*szCity*</span><span class="sxs-lookup"><span data-stu-id="68368-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-114">La ciudad del usuario.</span><span class="sxs-lookup"><span data-stu-id="68368-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="68368-115">*szCountry*</span><span class="sxs-lookup"><span data-stu-id="68368-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-116">País o región del usuario.</span><span class="sxs-lookup"><span data-stu-id="68368-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="68368-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="68368-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="68368-118">Valor que indica cómo se debe crear el certificado.</span><span class="sxs-lookup"><span data-stu-id="68368-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="68368-119">Los valores pueden ser cualquiera de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="68368-119">Values can be any of the following.</span></span>



| <span data-ttu-id="68368-120">Value</span><span class="sxs-lookup"><span data-stu-id="68368-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="68368-121">Significado</span><span class="sxs-lookup"><span data-stu-id="68368-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="68368-122"><dt>**NMMKCERT \_ \_ \_ Solo limpieza de F**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68368-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="68368-123">Elimine el certificado antiguo sin crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="68368-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="68368-124"><dt>**NMMKCERT \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="68368-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="68368-125">Elimine el certificado antiguo creado anteriormente con esta función.</span><span class="sxs-lookup"><span data-stu-id="68368-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="68368-126"><dt>**NMMKCERT \_ \_ \_ Máquina local de F**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="68368-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="68368-127">Cree el certificado en el almacén de certificados de la máquina local.</span><span class="sxs-lookup"><span data-stu-id="68368-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68368-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68368-128">Return value</span></span>

<span data-ttu-id="68368-129">Devuelve 1 si la función se ejecuta correctamente y – 1 si se produce un error en la función.</span><span class="sxs-lookup"><span data-stu-id="68368-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="68368-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68368-130">Remarks</span></span>

<span data-ttu-id="68368-131">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="68368-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="68368-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68368-132">Requirements</span></span>



| <span data-ttu-id="68368-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="68368-133">Requirement</span></span> | <span data-ttu-id="68368-134">Value</span><span class="sxs-lookup"><span data-stu-id="68368-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68368-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68368-135">DLL</span></span><br/> | <dl> <span data-ttu-id="68368-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68368-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
