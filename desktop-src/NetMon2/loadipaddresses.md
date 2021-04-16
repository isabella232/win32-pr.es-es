---
description: El monitor llama a la función LoadIPAddresses para rellenar una lista de direcciones IP con las direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Función LoadIPAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678575"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="09ce4-103">LoadIPAddresses función)</span><span class="sxs-lookup"><span data-stu-id="09ce4-103">LoadIPAddresses function</span></span>

<span data-ttu-id="09ce4-104">El monitor llama a la función **LoadIPAddresses** para rellenar una lista de direcciones IP con las direcciones tomadas de una variable de cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="09ce4-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ce4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09ce4-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="09ce4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ce4-107">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09ce4-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09ce4-108">Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.</span><span class="sxs-lookup"><span data-stu-id="09ce4-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="09ce4-109">*pVarName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09ce4-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09ce4-110">Puntero al nombre de la variable en la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="09ce4-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="09ce4-111">*ppAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="09ce4-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09ce4-112">Puntero a un puntero a una matriz de direcciones.</span><span class="sxs-lookup"><span data-stu-id="09ce4-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="09ce4-113">Si se encuentra la variable especificada en *pVarName* y tiene una longitud distinta de cero, la función asigna espacio suficiente y almacena todas las direcciones IP como una matriz.</span><span class="sxs-lookup"><span data-stu-id="09ce4-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="09ce4-114">*pNumAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="09ce4-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09ce4-115">Puntero a la variable **DWORD** que se establece en el número de direcciones IP tomadas de la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="09ce4-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ce4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09ce4-116">Return value</span></span>

<span data-ttu-id="09ce4-117">Si la función es correcta (se encontró el nombre de la variable y tenía una cadena que no es de longitud cero que representaba direcciones IP), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="09ce4-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="09ce4-118">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="09ce4-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09ce4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09ce4-119">Remarks</span></span>

<span data-ttu-id="09ce4-120">Las direcciones IP deben estar en formato x.x.x. x (por ejemplo, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="09ce4-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="09ce4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09ce4-121">Requirements</span></span>



| <span data-ttu-id="09ce4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ce4-122">Requirement</span></span> | <span data-ttu-id="09ce4-123">Value</span><span class="sxs-lookup"><span data-stu-id="09ce4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09ce4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09ce4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09ce4-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09ce4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="09ce4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09ce4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09ce4-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09ce4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="09ce4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09ce4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ce4-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ce4-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="09ce4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09ce4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="09ce4-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09ce4-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="09ce4-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09ce4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09ce4-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ce4-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




