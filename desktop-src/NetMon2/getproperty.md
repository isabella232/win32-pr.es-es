---
description: La función GetProperty devuelve un identificador a una propiedad determinada.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Función GetProperty (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000925"
---
# <a name="getproperty-function"></a><span data-ttu-id="dd943-103">GetProperty (función)</span><span class="sxs-lookup"><span data-stu-id="dd943-103">GetProperty function</span></span>

<span data-ttu-id="dd943-104">La función **GetProperty** devuelve un identificador a una propiedad determinada.</span><span class="sxs-lookup"><span data-stu-id="dd943-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd943-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd943-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="dd943-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd943-107">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd943-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd943-108">Identificador del protocolo.</span><span class="sxs-lookup"><span data-stu-id="dd943-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="dd943-109">*NombreDePropiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd943-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd943-110">Nombre de la propiedad (por ejemplo, **checksum**).</span><span class="sxs-lookup"><span data-stu-id="dd943-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd943-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd943-111">Return value</span></span>

<span data-ttu-id="dd943-112">Si la función se realiza correctamente, el valor devuelto es el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd943-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="dd943-113">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="dd943-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd943-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd943-114">Remarks</span></span>

<span data-ttu-id="dd943-115">La función **GetProperty** se puede usar para obtener el identificador de propiedad necesario para buscar las instancias de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dd943-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="dd943-116">Las funciones que se usan para buscar instancias de propiedad son [FindPropertyInstance](findpropertyinstance.md) (que localiza la primera instancia) y [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (que busca la instancia siguiente).</span><span class="sxs-lookup"><span data-stu-id="dd943-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="dd943-117">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProperty** .</span><span class="sxs-lookup"><span data-stu-id="dd943-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd943-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd943-118">Requirements</span></span>



| <span data-ttu-id="dd943-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd943-119">Requirement</span></span> | <span data-ttu-id="dd943-120">Value</span><span class="sxs-lookup"><span data-stu-id="dd943-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd943-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd943-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd943-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd943-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dd943-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd943-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd943-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd943-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd943-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd943-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd943-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd943-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="dd943-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd943-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd943-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd943-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="dd943-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd943-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd943-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd943-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd943-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd943-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd943-132">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="dd943-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="dd943-133">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="dd943-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




