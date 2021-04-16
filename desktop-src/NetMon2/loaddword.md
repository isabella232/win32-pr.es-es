---
description: El monitor llama a la función LoadDWORD para establecer una variable DWORD con un valor tomado de una variable de cadena de configuración HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Función LoadDWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678457"
---
# <a name="loaddword-function"></a><span data-ttu-id="160c3-103">LoadDWORD función)</span><span class="sxs-lookup"><span data-stu-id="160c3-103">LoadDWORD function</span></span>

<span data-ttu-id="160c3-104">El monitor llama a la función **LoadDWORD** para establecer una variable **DWORD** con un valor tomado de una variable de cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="160c3-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="160c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="160c3-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="160c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="160c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="160c3-107">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="160c3-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="160c3-108">Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.</span><span class="sxs-lookup"><span data-stu-id="160c3-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="160c3-109">*pVarName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="160c3-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="160c3-110">Puntero al nombre de la variable en la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="160c3-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="160c3-111">*pValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="160c3-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="160c3-112">Puntero a la variable **DWORD** que se establece en el valor de la variable de cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="160c3-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="160c3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="160c3-113">Return value</span></span>

<span data-ttu-id="160c3-114">Si la función es correcta (si se ha encontrado el nombre de la variable y tiene una cadena de longitud distinta de cero), se inserta el valor **DWORD** y el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="160c3-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="160c3-115">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="160c3-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="160c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="160c3-116">Requirements</span></span>



| <span data-ttu-id="160c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="160c3-117">Requirement</span></span> | <span data-ttu-id="160c3-118">Value</span><span class="sxs-lookup"><span data-stu-id="160c3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="160c3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="160c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="160c3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="160c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="160c3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="160c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="160c3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="160c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="160c3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="160c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="160c3-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="160c3-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="160c3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="160c3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="160c3-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="160c3-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="160c3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="160c3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="160c3-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="160c3-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




