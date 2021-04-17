---
description: Busca la función de destino de la importación especificada y reemplaza el puntero de función en el código thunk de importación con el destino de la implementación de función.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671120"
---
# <a name="resolvedelayloadedapi-function"></a><span data-ttu-id="79244-103">ResolveDelayLoadedAPI función)</span><span class="sxs-lookup"><span data-stu-id="79244-103">ResolveDelayLoadedAPI function</span></span>

<span data-ttu-id="79244-104">Busca la función de destino de la importación especificada y reemplaza el puntero de función en el código thunk de importación con el destino de la implementación de función.</span><span class="sxs-lookup"><span data-stu-id="79244-104">Locates the target function of the specified import and replaces the function pointer in the import thunk with the target of the function implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="79244-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79244-105">Syntax</span></span>


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="79244-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79244-107">*ParentModuleBase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79244-107">*ParentModuleBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79244-108">La dirección de la base del módulo que importa una función de carga retrasada.</span><span class="sxs-lookup"><span data-stu-id="79244-108">The address of the base of the module importing a delay-loaded function.</span></span>

</dd> <dt>

<span data-ttu-id="79244-109">*DelayloadDescriptor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79244-109">*DelayloadDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79244-110">Descriptor del módulo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="79244-110">The descriptor for the module to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="79244-111">*FailureDllHook* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="79244-111">*FailureDllHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79244-112">Dirección del enlace de error.</span><span class="sxs-lookup"><span data-stu-id="79244-112">The address of the failure hook.</span></span> <span data-ttu-id="79244-113">Vea [**DelayLoadFailureHook**](delayloadfailurehook.md).</span><span class="sxs-lookup"><span data-stu-id="79244-113">See [**DelayLoadFailureHook**](delayloadfailurehook.md).</span></span>

</dd> <dt>

<span data-ttu-id="79244-114">*FailureSystemHook* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="79244-114">*FailureSystemHook* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79244-115">Dirección del enlace de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="79244-115">The address of the system failure hook.</span></span>

</dd> <dt>

<span data-ttu-id="79244-116">*ThunkAddress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="79244-116">*ThunkAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79244-117">Los datos de thunk de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="79244-117">The thunk data for the target function.</span></span> <span data-ttu-id="79244-118">Se utiliza para buscar la entrada de la tabla de nombres específica de la función.</span><span class="sxs-lookup"><span data-stu-id="79244-118">Used to find the specific name table entry of the function.</span></span>

</dd> <dt>

<span data-ttu-id="79244-119">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="79244-119">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="79244-120">Sector debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="79244-120">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79244-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79244-121">Return value</span></span>

<span data-ttu-id="79244-122">La dirección de la importación o el código auxiliar de error correspondiente.</span><span class="sxs-lookup"><span data-stu-id="79244-122">The address of the import, or the failure stub for it.</span></span>

## <a name="requirements"></a><span data-ttu-id="79244-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79244-123">Requirements</span></span>



| <span data-ttu-id="79244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79244-124">Requirement</span></span> | <span data-ttu-id="79244-125">Value</span><span class="sxs-lookup"><span data-stu-id="79244-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79244-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79244-126">Library</span></span><br/> | <dl> <span data-ttu-id="79244-127"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="79244-127"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="79244-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79244-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="79244-129"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79244-129"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79244-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="79244-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="79244-131">[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="79244-131">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




