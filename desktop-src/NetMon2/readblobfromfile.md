---
description: La función ReadBlobFromFile Lee un BLOB en un archivo.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Función ReadBlobFromFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678516"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="27d08-103">ReadBlobFromFile función)</span><span class="sxs-lookup"><span data-stu-id="27d08-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="27d08-104">La función **ReadBlobFromFile** Lee un BLOB en un archivo.</span><span class="sxs-lookup"><span data-stu-id="27d08-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d08-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d08-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="27d08-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27d08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d08-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27d08-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d08-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="27d08-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="27d08-109">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27d08-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27d08-110">Puntero al nombre del archivo que contiene el BLOB.</span><span class="sxs-lookup"><span data-stu-id="27d08-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d08-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27d08-111">Return value</span></span>

<span data-ttu-id="27d08-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="27d08-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="27d08-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="27d08-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d08-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d08-114">Requirements</span></span>



| <span data-ttu-id="27d08-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d08-115">Requirement</span></span> | <span data-ttu-id="27d08-116">Value</span><span class="sxs-lookup"><span data-stu-id="27d08-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27d08-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d08-117">Minimum supported client</span></span><br/> | <span data-ttu-id="27d08-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27d08-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="27d08-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27d08-119">Minimum supported server</span></span><br/> | <span data-ttu-id="27d08-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27d08-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27d08-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27d08-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d08-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d08-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="27d08-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27d08-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="27d08-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27d08-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="27d08-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27d08-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27d08-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27d08-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




