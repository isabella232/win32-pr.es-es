---
description: Recupera los datos de atributo para el archivo especificado.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152704"
---
# <a name="sdbgetfileattributes-function"></a><span data-ttu-id="13e26-103">SdbGetFileAttributes función)</span><span class="sxs-lookup"><span data-stu-id="13e26-103">SdbGetFileAttributes function</span></span>

<span data-ttu-id="13e26-104">Recupera los datos de atributo para el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="13e26-104">Retrieves the attribute data for the specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e26-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13e26-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a><span data-ttu-id="13e26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13e26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e26-107">*lpwszFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13e26-107">*lpwszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e26-108">Ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="13e26-108">The path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="13e26-109">*ppAttrInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13e26-109">*ppAttrInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13e26-110">Matriz de estructuras [**ATTRINFO**](attrinfo.md) que contienen los datos del atributo.</span><span class="sxs-lookup"><span data-stu-id="13e26-110">An array of [**ATTRINFO**](attrinfo.md) structures that contain the attribute data.</span></span>

</dd> <dt>

<span data-ttu-id="13e26-111">*lpdwAttrCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13e26-111">*lpdwAttrCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13e26-112">Número de atributos.</span><span class="sxs-lookup"><span data-stu-id="13e26-112">The number of attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13e26-113">Return value</span></span>

<span data-ttu-id="13e26-114">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="13e26-114">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e26-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13e26-115">Remarks</span></span>

<span data-ttu-id="13e26-116">Cuando haya terminado con los datos, libere el uso de la función [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="13e26-116">When you have finished with the data, free it using the [**SdbFreeFileAttributes**](sdbfreefileattributes.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e26-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13e26-117">Requirements</span></span>



| <span data-ttu-id="13e26-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e26-118">Requirement</span></span> | <span data-ttu-id="13e26-119">Value</span><span class="sxs-lookup"><span data-stu-id="13e26-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e26-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13e26-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13e26-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13e26-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="13e26-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13e26-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13e26-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="13e26-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13e26-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13e26-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e26-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e26-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e26-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="13e26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e26-127">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="13e26-127">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="13e26-128">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="13e26-128">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> </dl>

 

 




