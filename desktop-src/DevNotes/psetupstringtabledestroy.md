---
description: Elimina una tabla de cadenas.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670517"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="b3230-103">pSetupStringTableDestroy función)</span><span class="sxs-lookup"><span data-stu-id="b3230-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="b3230-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="b3230-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="b3230-105">Elimina una tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="b3230-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3230-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3230-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="b3230-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3230-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3230-108">*StringTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3230-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3230-109">Puntero a la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="b3230-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3230-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3230-110">Return value</span></span>

<span data-ttu-id="b3230-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b3230-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3230-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3230-112">Remarks</span></span>

<span data-ttu-id="b3230-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b3230-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3230-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3230-114">Requirements</span></span>



| <span data-ttu-id="b3230-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3230-115">Requirement</span></span> | <span data-ttu-id="b3230-116">Value</span><span class="sxs-lookup"><span data-stu-id="b3230-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3230-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3230-117">DLL</span></span><br/> | <dl> <span data-ttu-id="b3230-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3230-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
