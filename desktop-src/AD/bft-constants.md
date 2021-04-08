---
title: Constantes BFT (Ntdsbcli. h)
description: Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de seguridad de Active Directory Domain Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996236"
---
# <a name="bft-constants"></a><span data-ttu-id="f43c6-103">Constantes de BFT</span><span class="sxs-lookup"><span data-stu-id="f43c6-103">BFT Constants</span></span>

<span data-ttu-id="f43c6-104">Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de seguridad de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f43c6-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="f43c6-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_Directorio de registro de BFT \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-106">0x20</span><span class="sxs-lookup"><span data-stu-id="f43c6-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-107">El archivo pertenece al directorio de registro.</span><span class="sxs-lookup"><span data-stu-id="f43c6-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Directorio de base de datos BFT \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-109">0x40</span><span class="sxs-lookup"><span data-stu-id="f43c6-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-110">El archivo pertenece al directorio de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f43c6-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_directorio BFT**</span><span class="sxs-lookup"><span data-stu-id="f43c6-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-112">0x80</span><span class="sxs-lookup"><span data-stu-id="f43c6-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-113">La ruta de acceso especificada es un directorio y no un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f43c6-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**registro de BFT \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-115">0x21</span><span class="sxs-lookup"><span data-stu-id="f43c6-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-116">Especifica un archivo de registro que pertenece al directorio de registro.</span><span class="sxs-lookup"><span data-stu-id="f43c6-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**DIR. de registro de BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-118">0x22</span><span class="sxs-lookup"><span data-stu-id="f43c6-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-119">El archivo es la ruta de acceso del directorio de registro.</span><span class="sxs-lookup"><span data-stu-id="f43c6-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR. de punto de BFT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-121">0x23</span><span class="sxs-lookup"><span data-stu-id="f43c6-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-122">El archivo es la ruta de acceso del directorio Checkpoint.</span><span class="sxs-lookup"><span data-stu-id="f43c6-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**</span><span class="sxs-lookup"><span data-stu-id="f43c6-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-124">0X44</span><span class="sxs-lookup"><span data-stu-id="f43c6-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-125">El archivo es una base de datos del servicio de directorio que pertenece al directorio de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f43c6-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_archivo de revisión BFT \_**</span><span class="sxs-lookup"><span data-stu-id="f43c6-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-127">0x25</span><span class="sxs-lookup"><span data-stu-id="f43c6-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-128">El archivo es un archivo de revisión que pertenece al directorio de registro.</span><span class="sxs-lookup"><span data-stu-id="f43c6-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f43c6-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="f43c6-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f43c6-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="f43c6-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="f43c6-131">No se reconoce el archivo.</span><span class="sxs-lookup"><span data-stu-id="f43c6-131">The file cannot be recognized.</span></span> <span data-ttu-id="f43c6-132">El archivo no coincide con los nombres de archivo y los tipos de archivo conocidos.</span><span class="sxs-lookup"><span data-stu-id="f43c6-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f43c6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f43c6-133">Requirements</span></span>



| <span data-ttu-id="f43c6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f43c6-134">Requirement</span></span> | <span data-ttu-id="f43c6-135">Value</span><span class="sxs-lookup"><span data-stu-id="f43c6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f43c6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f43c6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f43c6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f43c6-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="f43c6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f43c6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f43c6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f43c6-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="f43c6-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f43c6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f43c6-141"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f43c6-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





