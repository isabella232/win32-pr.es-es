---
description: Escribe datos binarios del archivo especificado en la base de datos especificada.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998204"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="0b034-103">SdbWriteBinaryTagFromFile función)</span><span class="sxs-lookup"><span data-stu-id="0b034-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="0b034-104">Escribe datos binarios del archivo especificado en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="0b034-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b034-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b034-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="0b034-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b034-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b034-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b034-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b034-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="0b034-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0b034-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b034-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b034-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="0b034-110">The TAG for the entry.</span></span> <span data-ttu-id="0b034-111">Esta etiqueta debe ser de tipo **etiqueta \_ \_ binaria**.</span><span class="sxs-lookup"><span data-stu-id="0b034-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="0b034-112">*pwszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b034-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b034-113">Ruta de acceso al archivo que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="0b034-113">The path to the file that contains the data.</span></span> <span data-ttu-id="0b034-114">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="0b034-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b034-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b034-115">Return value</span></span>

<span data-ttu-id="0b034-116">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="0b034-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b034-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b034-117">Requirements</span></span>



| <span data-ttu-id="0b034-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b034-118">Requirement</span></span> | <span data-ttu-id="0b034-119">Value</span><span class="sxs-lookup"><span data-stu-id="0b034-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b034-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b034-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b034-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0b034-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0b034-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b034-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b034-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b034-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b034-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b034-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b034-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b034-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b034-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b034-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b034-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="0b034-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




