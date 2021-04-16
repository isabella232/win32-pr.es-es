---
description: Los monitores llaman a la función LoadTCHAR para establecer una variable de cadena en una cadena tomada de una cadena de configuración HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Función LoadTCHAR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677413"
---
# <a name="loadtchar-function"></a><span data-ttu-id="c21e8-103">LoadTCHAR función)</span><span class="sxs-lookup"><span data-stu-id="c21e8-103">LoadTCHAR function</span></span>

<span data-ttu-id="c21e8-104">Los monitores llaman a la función **LoadTCHAR** para establecer una variable de cadena en una cadena tomada de una cadena de configuración HTML.</span><span class="sxs-lookup"><span data-stu-id="c21e8-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c21e8-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="c21e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c21e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21e8-107">*pConfig* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c21e8-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c21e8-108">Puntero a la cadena de configuración HTML que el método [IMonitor::D oconfigure](imonitor-doconfigure.md) pasa al monitor.</span><span class="sxs-lookup"><span data-stu-id="c21e8-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="c21e8-109">*pVarName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c21e8-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c21e8-110">Puntero al nombre de la variable en la cadena de configuración.</span><span class="sxs-lookup"><span data-stu-id="c21e8-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="c21e8-111">*ppszString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c21e8-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c21e8-112">Puntero a un puntero de cadena.</span><span class="sxs-lookup"><span data-stu-id="c21e8-112">Pointer to a string pointer.</span></span> <span data-ttu-id="c21e8-113">Si se encuentra el nombre de la variable solicitada, la cadena se asigna y se asigna a este puntero.</span><span class="sxs-lookup"><span data-stu-id="c21e8-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="c21e8-114">Es responsable del usuario la liberación de la memoria asociada a la cadena.</span><span class="sxs-lookup"><span data-stu-id="c21e8-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21e8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c21e8-115">Return value</span></span>

<span data-ttu-id="c21e8-116">Si la función es correcta (si se ha encontrado el nombre de la variable y tiene una cadena de longitud distinta de cero), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="c21e8-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="c21e8-117">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="c21e8-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c21e8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c21e8-118">Requirements</span></span>



| <span data-ttu-id="c21e8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c21e8-119">Requirement</span></span> | <span data-ttu-id="c21e8-120">Value</span><span class="sxs-lookup"><span data-stu-id="c21e8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c21e8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c21e8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c21e8-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c21e8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c21e8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c21e8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c21e8-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c21e8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c21e8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c21e8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21e8-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c21e8-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c21e8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c21e8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c21e8-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c21e8-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c21e8-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c21e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c21e8-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c21e8-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




