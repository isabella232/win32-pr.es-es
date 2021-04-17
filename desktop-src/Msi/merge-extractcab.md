---
description: El método ExtractCAB del objeto Merge extrae el archivo. cab incrustado de un módulo y lo guarda como el archivo especificado. El instalador crea este archivo si aún no existe y se sobrescribe si existe.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Método Merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670452"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="38bc8-104">Merge. ExtractCAB (método)</span><span class="sxs-lookup"><span data-stu-id="38bc8-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="38bc8-105">El método **ExtractCAB** del objeto [**Merge**](merge-object.md) extrae el archivo. cab incrustado de un módulo y lo guarda como el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="38bc8-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="38bc8-106">El instalador crea este archivo si aún no existe y se sobrescribe si existe.</span><span class="sxs-lookup"><span data-stu-id="38bc8-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="38bc8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38bc8-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="38bc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38bc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38bc8-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="38bc8-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="38bc8-110">El archivo de destino completo.</span><span class="sxs-lookup"><span data-stu-id="38bc8-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38bc8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38bc8-111">Return value</span></span>

<span data-ttu-id="38bc8-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="38bc8-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="38bc8-113">C++</span><span class="sxs-lookup"><span data-stu-id="38bc8-113">C++</span></span>

<span data-ttu-id="38bc8-114">Consulte función [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .</span><span class="sxs-lookup"><span data-stu-id="38bc8-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38bc8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38bc8-115">Requirements</span></span>



| <span data-ttu-id="38bc8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38bc8-116">Requirement</span></span> | <span data-ttu-id="38bc8-117">Value</span><span class="sxs-lookup"><span data-stu-id="38bc8-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38bc8-118">Versión</span><span class="sxs-lookup"><span data-stu-id="38bc8-118">Version</span></span><br/> | <span data-ttu-id="38bc8-119">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="38bc8-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="38bc8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38bc8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="38bc8-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="38bc8-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="38bc8-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38bc8-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="38bc8-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38bc8-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
