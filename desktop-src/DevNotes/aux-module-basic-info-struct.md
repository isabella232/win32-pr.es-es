---
description: Contiene información básica del módulo.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: AUX_MODULE_BASIC_INFO estructura (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649967"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="669f6-103">\_Estructura de \_ información básica del módulo AUX \_</span><span class="sxs-lookup"><span data-stu-id="669f6-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="669f6-104">Contiene información básica del módulo.</span><span class="sxs-lookup"><span data-stu-id="669f6-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="669f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="669f6-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="669f6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="669f6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="669f6-107">**ImageBase**</span><span class="sxs-lookup"><span data-stu-id="669f6-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="669f6-108">La dirección base del módulo dentro del espacio de direcciones del kernel.</span><span class="sxs-lookup"><span data-stu-id="669f6-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="669f6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="669f6-109">Remarks</span></span>

<span data-ttu-id="669f6-110">La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="669f6-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="669f6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="669f6-111">Requirements</span></span>



| <span data-ttu-id="669f6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="669f6-112">Requirement</span></span> | <span data-ttu-id="669f6-113">Value</span><span class="sxs-lookup"><span data-stu-id="669f6-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="669f6-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="669f6-114">Redistributable</span></span><br/> | <span data-ttu-id="669f6-115">Biblioteca de API auxiliar de Windows versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="669f6-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="669f6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="669f6-116">Header</span></span><br/>          | <dl> <span data-ttu-id="669f6-117"><dt>AUX \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="669f6-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="669f6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="669f6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="669f6-119">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="669f6-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




