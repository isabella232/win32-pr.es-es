---
title: Método CreateUserDiskTemplate de la clase Win32_TSSessionDirectory
description: Crea una plantilla de disco de usuario.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Método CreateUserDiskTemplate Servicios de Escritorio remoto
- Método CreateUserDiskTemplate Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150002"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="9c978-106">Método CreateUserDiskTemplate de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="9c978-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="9c978-107">Crea una plantilla de disco de usuario.</span><span class="sxs-lookup"><span data-stu-id="9c978-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c978-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c978-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="9c978-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c978-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c978-110">*UserDisksStorageUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c978-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c978-111">La ubicación del recurso compartido donde se almacenan todos los discos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9c978-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="9c978-112">*UserDiskMaxSizeInGB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c978-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c978-113">El tamaño máximo en gigabytes, para todos los discos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9c978-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c978-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c978-114">Requirements</span></span>



| <span data-ttu-id="9c978-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c978-115">Requirement</span></span> | <span data-ttu-id="9c978-116">Value</span><span class="sxs-lookup"><span data-stu-id="9c978-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c978-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c978-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c978-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c978-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9c978-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c978-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c978-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c978-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="9c978-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c978-121">Namespace</span></span><br/>                | <span data-ttu-id="9c978-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9c978-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9c978-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9c978-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c978-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c978-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c978-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c978-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c978-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c978-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c978-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c978-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c978-128">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="9c978-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





