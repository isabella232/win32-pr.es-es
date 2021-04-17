---
description: Invoca la funcionalidad auxiliar para la interfaz IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706573"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="25049-103">InvokeIDispatch función)</span><span class="sxs-lookup"><span data-stu-id="25049-103">InvokeIDispatch function</span></span>

<span data-ttu-id="25049-104">Invoca la funcionalidad auxiliar para la interfaz IDispatch.</span><span class="sxs-lookup"><span data-stu-id="25049-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="25049-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="25049-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="25049-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25049-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="25049-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25049-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25049-108">*pDispatch*</span><span class="sxs-lookup"><span data-stu-id="25049-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="25049-109">Instancia de la interfaz IDispatch.</span><span class="sxs-lookup"><span data-stu-id="25049-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="25049-110">*DISPID*</span><span class="sxs-lookup"><span data-stu-id="25049-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="25049-111">Método, propiedad o argumento que se va a pasar.</span><span class="sxs-lookup"><span data-stu-id="25049-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="25049-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="25049-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="25049-113">Parámetros que se van a pasar.</span><span class="sxs-lookup"><span data-stu-id="25049-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="25049-114">*pVarResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="25049-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25049-115">Estructura que recibe los valores recuperados.</span><span class="sxs-lookup"><span data-stu-id="25049-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25049-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25049-116">Return value</span></span>

<span data-ttu-id="25049-117">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="25049-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="25049-118">Si se produce un error, los códigos de retorno posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="25049-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="25049-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25049-119">Return code</span></span>                                                                                  | <span data-ttu-id="25049-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="25049-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="25049-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25049-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="25049-122">El valor de *pDispatch* no es válido.</span><span class="sxs-lookup"><span data-stu-id="25049-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="25049-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25049-123">Requirements</span></span>



| <span data-ttu-id="25049-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25049-124">Requirement</span></span> | <span data-ttu-id="25049-125">Value</span><span class="sxs-lookup"><span data-stu-id="25049-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25049-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25049-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25049-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="25049-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="25049-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25049-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25049-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25049-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="25049-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25049-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="25049-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25049-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




