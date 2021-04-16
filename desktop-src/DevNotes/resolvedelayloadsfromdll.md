---
description: Reenvía el trabajo en la resolución de las importaciones de carga retrasada del archivo binario primario a un binario de destino.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671625"
---
# <a name="resolvedelayloadsfromdll-function"></a><span data-ttu-id="c78cf-103">ResolveDelayLoadsFromDll función)</span><span class="sxs-lookup"><span data-stu-id="c78cf-103">ResolveDelayLoadsFromDll function</span></span>

<span data-ttu-id="c78cf-104">Reenvía el trabajo en la resolución de las importaciones de carga retrasada del archivo binario primario a un binario de destino.</span><span class="sxs-lookup"><span data-stu-id="c78cf-104">Forwards the work in resolving delay-loaded imports from the parent binary to a target binary.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c78cf-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c78cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c78cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c78cf-107">*ParentBase* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c78cf-107">*ParentBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78cf-108">La dirección base del módulo que retrasa la carga otro binario.</span><span class="sxs-lookup"><span data-stu-id="c78cf-108">The base address of the module that delay loads another binary.</span></span>

</dd> <dt>

<span data-ttu-id="c78cf-109">*TargetDllName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c78cf-109">*TargetDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c78cf-110">Nombre del archivo DLL de destino.</span><span class="sxs-lookup"><span data-stu-id="c78cf-110">The name of the target DLL.</span></span>

</dd> <dt>

<span data-ttu-id="c78cf-111">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="c78cf-111">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="c78cf-112">Sector debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="c78cf-112">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c78cf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c78cf-113">Return value</span></span>

<span data-ttu-id="c78cf-114">La dirección del descriptor de carga retrasada, si se encuentra; de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="c78cf-114">The address of the delay-load descriptor, if it is found; otherwise, **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c78cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c78cf-115">Requirements</span></span>



| <span data-ttu-id="c78cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c78cf-116">Requirement</span></span> | <span data-ttu-id="c78cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="c78cf-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c78cf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c78cf-118">Library</span></span><br/> | <dl> <span data-ttu-id="c78cf-119"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c78cf-119"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c78cf-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c78cf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c78cf-121"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c78cf-121"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c78cf-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c78cf-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c78cf-123">[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="c78cf-123">[Linker Support for Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




