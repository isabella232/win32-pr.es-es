---
description: El monitor llama a la función LoadIPXAddresses para rellenar una lista de direcciones IPX tomada de una variable de cadena de configuración HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Función LoadIPXAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278604"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="d480d-103">LoadIPXAddresses función)</span><span class="sxs-lookup"><span data-stu-id="d480d-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="d480d-104">El monitor llama a la función **LoadIPXAddresses** para rellenar una lista de direcciones IPX tomada de una variable de cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="d480d-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d480d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d480d-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="d480d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d480d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d480d-107">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d480d-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d480d-108">Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.</span><span class="sxs-lookup"><span data-stu-id="d480d-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="d480d-109">*pVarName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d480d-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d480d-110">Puntero al nombre de la variable en la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="d480d-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="d480d-111">*ppAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d480d-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d480d-112">Puntero a un puntero a una matriz de direcciones.</span><span class="sxs-lookup"><span data-stu-id="d480d-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="d480d-113">Si se encuentra la variable especificada en *pVarName* y tiene una longitud distinta de cero, se asigna espacio suficiente (mediante **HeapAllocMemory**) y todas las direcciones IPX se almacenan como una matriz.</span><span class="sxs-lookup"><span data-stu-id="d480d-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="d480d-114">*pNumAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d480d-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d480d-115">Puntero a la variable **DWORD** que se establece en el número de direcciones IPX tomadas de la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="d480d-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d480d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d480d-116">Return value</span></span>

<span data-ttu-id="d480d-117">Si la función es correcta (se encontró el nombre de la variable y tenía una cadena que no es de longitud cero que representaba direcciones IPX), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="d480d-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="d480d-118">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="d480d-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d480d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d480d-119">Requirements</span></span>



| <span data-ttu-id="d480d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d480d-120">Requirement</span></span> | <span data-ttu-id="d480d-121">Value</span><span class="sxs-lookup"><span data-stu-id="d480d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d480d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d480d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d480d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d480d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d480d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d480d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d480d-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d480d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d480d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d480d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d480d-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d480d-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d480d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d480d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d480d-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d480d-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d480d-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d480d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d480d-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d480d-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




