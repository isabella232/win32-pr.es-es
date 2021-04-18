---
description: El método Connect del objeto Merge conecta un módulo con una característica adicional. El módulo se debe haber combinado ya en la base de datos o se combinará en la base de datos. La característica debe existir antes de llamar a esta función.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Merge. Connect (método) (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670743"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="cde33-105">Merge. Connect (método)</span><span class="sxs-lookup"><span data-stu-id="cde33-105">Merge.Connect method</span></span>

<span data-ttu-id="cde33-106">El método **Connect** del objeto [**Merge**](merge-object.md) conecta un módulo con una característica adicional.</span><span class="sxs-lookup"><span data-stu-id="cde33-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="cde33-107">El módulo se debe haber combinado ya en la base de datos o se combinará en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cde33-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="cde33-108">La característica debe existir antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="cde33-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="cde33-109">Los cambios realizados en la base de datos no se guardan en el disco a menos que se llame al método [**CerrarBaseDeDatos**](merge-closedatabase.md) con *BCommit* establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="cde33-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde33-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cde33-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="cde33-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cde33-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde33-112">*Característica*</span><span class="sxs-lookup"><span data-stu-id="cde33-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="cde33-113">Nombre de una característica que ya existe en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cde33-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde33-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cde33-114">Return value</span></span>

<span data-ttu-id="cde33-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cde33-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde33-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cde33-116">Remarks</span></span>

<span data-ttu-id="cde33-117">Los errores se pueden recuperar a través de la propiedad [**errores**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="cde33-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="cde33-118">Los errores y los mensajes informativos se publican en el archivo de registro actual.</span><span class="sxs-lookup"><span data-stu-id="cde33-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="cde33-119">C++</span><span class="sxs-lookup"><span data-stu-id="cde33-119">C++</span></span>

<span data-ttu-id="cde33-120">Vea [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) (función).</span><span class="sxs-lookup"><span data-stu-id="cde33-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde33-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde33-121">Requirements</span></span>



| <span data-ttu-id="cde33-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde33-122">Requirement</span></span> | <span data-ttu-id="cde33-123">Value</span><span class="sxs-lookup"><span data-stu-id="cde33-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde33-124">Versión</span><span class="sxs-lookup"><span data-stu-id="cde33-124">Version</span></span><br/> | <span data-ttu-id="cde33-125">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cde33-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="cde33-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cde33-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cde33-127"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde33-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="cde33-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cde33-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="cde33-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde33-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
