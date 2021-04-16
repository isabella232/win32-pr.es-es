---
description: Recupera el estado de la memoria caché de Archivos sin conexión.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650064"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="7fa0c-103">CSCQueryDatabaseStatus función)</span><span class="sxs-lookup"><span data-stu-id="7fa0c-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="7fa0c-104">\[Esta función no se admite y no debe usarse.\]</span><span class="sxs-lookup"><span data-stu-id="7fa0c-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="7fa0c-105">Recupera el estado de la memoria caché de Archivos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa0c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fa0c-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7fa0c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fa0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fa0c-108">*pulStatus*</span><span class="sxs-lookup"><span data-stu-id="7fa0c-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="7fa0c-109">Estado.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-109">The status.</span></span> <span data-ttu-id="7fa0c-110">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7fa0c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa0c-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="7fa0c-112">Significado</span><span class="sxs-lookup"><span data-stu-id="7fa0c-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="7fa0c-113"><dt>**Marca \_ de DATABASESTATUS \_ cifrado**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="7fa0c-114">La memoria caché está marcada para el cifrado y se cifran todos los archivos de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="7fa0c-115"><dt>**Marca \_ de DATABASESTATUS el 0x00000004 \_ parcialmente \_ cifrado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="7fa0c-116">La memoria caché está marcada para el cifrado, pero algunos archivos de la memoria caché no están cifrados.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="7fa0c-117"><dt>**Marca \_ de DATABASESTATUS \_ parcialmente \_ descifrado**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="7fa0c-118">La memoria caché no está marcada para el cifrado, pero no se han descifrado todos los archivos de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="7fa0c-119"><dt>**Marca \_ de DATABASESTATUS \_ sin cifrar**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="7fa0c-120">La memoria caché no está marcada para el cifrado y se han descifrado todos los archivos de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="7fa0c-121">*pulErrors*</span><span class="sxs-lookup"><span data-stu-id="7fa0c-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="7fa0c-122">Este parámetro es un valor distinto de cero si hay un error interno de la base de datos o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fa0c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fa0c-123">Return value</span></span>

<span data-ttu-id="7fa0c-124">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7fa0c-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa0c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fa0c-125">Remarks</span></span>

<span data-ttu-id="7fa0c-126">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7fa0c-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa0c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa0c-127">Requirements</span></span>



| <span data-ttu-id="7fa0c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa0c-128">Requirement</span></span> | <span data-ttu-id="7fa0c-129">Value</span><span class="sxs-lookup"><span data-stu-id="7fa0c-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa0c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fa0c-130">DLL</span></span><br/> | <dl> <span data-ttu-id="7fa0c-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fa0c-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa0c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fa0c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa0c-133">**CSCIsCSCEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fa0c-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
