---
description: Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para la DLL y el proceso especificados.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660494"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="6b701-103">DelayLoadFailureHook función)</span><span class="sxs-lookup"><span data-stu-id="6b701-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="6b701-104">Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para la DLL y el proceso especificados.</span><span class="sxs-lookup"><span data-stu-id="6b701-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b701-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b701-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="6b701-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b701-107">*pszDllName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b701-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b701-108">Nombre del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="6b701-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="6b701-109">*pszProcName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b701-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b701-110">Nombre del proceso.</span><span class="sxs-lookup"><span data-stu-id="6b701-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b701-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b701-111">Return value</span></span>

<span data-ttu-id="6b701-112">Dirección de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6b701-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b701-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b701-113">Requirements</span></span>



| <span data-ttu-id="6b701-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b701-114">Requirement</span></span> | <span data-ttu-id="6b701-115">Value</span><span class="sxs-lookup"><span data-stu-id="6b701-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b701-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b701-116">Library</span></span><br/> | <dl> <span data-ttu-id="6b701-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b701-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b701-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b701-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b701-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b701-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b701-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b701-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b701-121">[Enlaces de error](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="6b701-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




