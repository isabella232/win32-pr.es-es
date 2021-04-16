---
description: El monitor llama a la función LoadMACAddresses para rellenar una lista de direcciones MAC con las direcciones tomadas de una variable de cadena de configuración HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Función LoadMACAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542382"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="aa4da-103">LoadMACAddresses función)</span><span class="sxs-lookup"><span data-stu-id="aa4da-103">LoadMACAddresses function</span></span>

<span data-ttu-id="aa4da-104">El monitor llama a la función **LoadMACAddresses** para rellenar una lista de direcciones MAC con las direcciones tomadas de una variable de cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="aa4da-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa4da-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="aa4da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa4da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4da-107">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa4da-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4da-108">Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.</span><span class="sxs-lookup"><span data-stu-id="aa4da-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="aa4da-109">*pVarName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa4da-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4da-110">Puntero al nombre de la variable en la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="aa4da-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="aa4da-111">*ppAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa4da-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4da-112">Puntero a un puntero a una matriz de direcciones.</span><span class="sxs-lookup"><span data-stu-id="aa4da-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="aa4da-113">Si se encuentra la variable especificada en *pVarName* y tiene una longitud distinta de cero, la función asigna espacio suficiente (mediante **HeapAllocMemory**) y almacena todas las direcciones MAC como una matriz.</span><span class="sxs-lookup"><span data-stu-id="aa4da-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="aa4da-114">*pNumAddresses* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa4da-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa4da-115">Puntero a la variable **DWORD** que se establece en el número de direcciones MAC tomadas de la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="aa4da-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4da-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa4da-116">Return value</span></span>

<span data-ttu-id="aa4da-117">Si la función es correcta, se encontró el nombre de la variable y tenía una cadena que no es de longitud cero que representaba direcciones MAC), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="aa4da-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="aa4da-118">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="aa4da-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4da-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4da-119">Requirements</span></span>



| <span data-ttu-id="aa4da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4da-120">Requirement</span></span> | <span data-ttu-id="aa4da-121">Value</span><span class="sxs-lookup"><span data-stu-id="aa4da-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4da-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa4da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4da-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa4da-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa4da-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa4da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4da-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa4da-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa4da-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa4da-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4da-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4da-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="aa4da-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa4da-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa4da-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa4da-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa4da-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa4da-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa4da-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa4da-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




