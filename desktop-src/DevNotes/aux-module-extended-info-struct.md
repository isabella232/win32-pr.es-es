---
description: Contiene información del módulo extendido.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: AUX_MODULE_EXTENDED_INFO estructura (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650070"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="a836d-103">\_Estructura de \_ información ampliada del módulo AUX \_</span><span class="sxs-lookup"><span data-stu-id="a836d-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="a836d-104">Contiene información del módulo extendido.</span><span class="sxs-lookup"><span data-stu-id="a836d-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a836d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a836d-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="a836d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a836d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a836d-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="a836d-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="a836d-108">Una estructura de [**\_ \_ \_ información básica del módulo AUX**](aux-module-basic-info-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="a836d-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a836d-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="a836d-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="a836d-110">Tamaño, en bytes, del módulo cargado.</span><span class="sxs-lookup"><span data-stu-id="a836d-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="a836d-111">**FileNameOffset**</span><span class="sxs-lookup"><span data-stu-id="a836d-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a836d-112">Desplazamiento del nombre de archivo dentro del búfer de **FullPathName** .</span><span class="sxs-lookup"><span data-stu-id="a836d-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a836d-113">**FullPathName**</span><span class="sxs-lookup"><span data-stu-id="a836d-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="a836d-114">Ruta de acceso completa del módulo.</span><span class="sxs-lookup"><span data-stu-id="a836d-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a836d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a836d-115">Remarks</span></span>

<span data-ttu-id="a836d-116">La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="a836d-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="a836d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a836d-117">Requirements</span></span>



| <span data-ttu-id="a836d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a836d-118">Requirement</span></span> | <span data-ttu-id="a836d-119">Value</span><span class="sxs-lookup"><span data-stu-id="a836d-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a836d-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a836d-120">Redistributable</span></span><br/> | <span data-ttu-id="a836d-121">Biblioteca de API auxiliar de Windows versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a836d-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="a836d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a836d-122">Header</span></span><br/>          | <dl> <span data-ttu-id="a836d-123"><dt>AUX \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="a836d-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a836d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a836d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a836d-125">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="a836d-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="a836d-126">**\_ \_ información básica del módulo AUX \_**</span><span class="sxs-lookup"><span data-stu-id="a836d-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




