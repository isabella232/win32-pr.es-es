---
description: La función RemoveFromBlob elimina cualquier nivel de entrada de BLOB (propietario, categoría o etiqueta).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Función RemoveFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677347"
---
# <a name="removefromblob-function"></a><span data-ttu-id="1e049-103">RemoveFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="1e049-103">RemoveFromBlob function</span></span>

<span data-ttu-id="1e049-104">La función **RemoveFromBlob** elimina cualquier nivel de entrada de BLOB (**propietario**, **categoría** o **etiqueta**).</span><span class="sxs-lookup"><span data-stu-id="1e049-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e049-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e049-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="1e049-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e049-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e049-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e049-108">Identificador del BLOB del que se elimina una entrada.</span><span class="sxs-lookup"><span data-stu-id="1e049-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="1e049-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e049-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e049-110">Puntero al nombre del **propietario** .</span><span class="sxs-lookup"><span data-stu-id="1e049-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="1e049-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e049-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e049-112">Puntero al nombre de la **categoría** .</span><span class="sxs-lookup"><span data-stu-id="1e049-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="1e049-113">Un valor de parámetro **null** indica que el autor de la llamada está intentando eliminar la información de **propietario** especificada y todas sus entradas secundarias.</span><span class="sxs-lookup"><span data-stu-id="1e049-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="1e049-114">Tenga en cuenta que si el valor del parámetro *pCategoryName* es **null**, el parámetro *pTagName* también debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1e049-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1e049-115">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e049-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e049-116">Puntero al nombre de la **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="1e049-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="1e049-117">Un valor _PTagName_ **nulo** indica que el autor de la llamada está intentando eliminar la **categoría** especificada y todas sus entradas secundarias.</span><span class="sxs-lookup"><span data-stu-id="1e049-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="1e049-118">Si el valor del parámetro no es **null**, el autor de la llamada solicita que solo se eliminen las entradas especificadas de la **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="1e049-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e049-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e049-119">Return value</span></span>

<span data-ttu-id="1e049-120">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1e049-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1e049-121">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="1e049-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e049-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e049-122">Requirements</span></span>



| <span data-ttu-id="1e049-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e049-123">Requirement</span></span> | <span data-ttu-id="1e049-124">Value</span><span class="sxs-lookup"><span data-stu-id="1e049-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e049-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e049-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e049-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e049-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e049-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e049-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e049-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e049-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e049-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e049-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e049-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e049-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1e049-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e049-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e049-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e049-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e049-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e049-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e049-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e049-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




