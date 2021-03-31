---
title: Método GetIcon de la clase Win32_TSGetIcon
description: Devuelve el contenido del icono especificado.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Método GetIcon Servicios de Escritorio remoto
- Método GetIcon Servicios de Escritorio remoto, clase Win32_TSGetIcon
- Win32_TSGetIcon de clase Servicios de Escritorio remoto, método GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996019"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="9c32a-106">Método GetIcon de la \_ clase TSGetIcon de Win32</span><span class="sxs-lookup"><span data-stu-id="9c32a-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="9c32a-107">Devuelve el contenido del icono especificado.</span><span class="sxs-lookup"><span data-stu-id="9c32a-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c32a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c32a-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="9c32a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c32a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c32a-110">*FilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c32a-111">Especifica la ruta de acceso al archivo que contiene el icono.</span><span class="sxs-lookup"><span data-stu-id="9c32a-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="9c32a-112">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c32a-113">Especifica el índice del icono en el archivo.</span><span class="sxs-lookup"><span data-stu-id="9c32a-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="9c32a-114">*IconContents* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c32a-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c32a-115">Al finalizar correctamente, se incluye el contenido del icono.</span><span class="sxs-lookup"><span data-stu-id="9c32a-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c32a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c32a-116">Requirements</span></span>



| <span data-ttu-id="9c32a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c32a-117">Requirement</span></span> | <span data-ttu-id="9c32a-118">Value</span><span class="sxs-lookup"><span data-stu-id="9c32a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c32a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c32a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c32a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c32a-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9c32a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c32a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c32a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c32a-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="9c32a-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c32a-123">Namespace</span></span><br/>                | <span data-ttu-id="9c32a-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9c32a-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9c32a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="9c32a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c32a-126"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c32a-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="9c32a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c32a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c32a-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c32a-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c32a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c32a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c32a-130">**Win32 \_ TSGetIcon**</span><span class="sxs-lookup"><span data-stu-id="9c32a-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





