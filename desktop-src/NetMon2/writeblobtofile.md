---
description: La función WriteBlobToFile escribe un BLOB en un archivo.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Función WriteBlobToFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668062"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="d2f78-103">WriteBlobToFile función)</span><span class="sxs-lookup"><span data-stu-id="d2f78-103">WriteBlobToFile function</span></span>

<span data-ttu-id="d2f78-104">La función **WriteBlobToFile** escribe un BLOB en un archivo.</span><span class="sxs-lookup"><span data-stu-id="d2f78-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2f78-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d2f78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2f78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f78-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2f78-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f78-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2f78-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="d2f78-109">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2f78-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f78-110">Puntero al nombre del archivo en el que se guarda el BLOB.</span><span class="sxs-lookup"><span data-stu-id="d2f78-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f78-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2f78-111">Return value</span></span>

<span data-ttu-id="d2f78-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d2f78-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d2f78-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="d2f78-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f78-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f78-114">Requirements</span></span>



| <span data-ttu-id="d2f78-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f78-115">Requirement</span></span> | <span data-ttu-id="d2f78-116">Value</span><span class="sxs-lookup"><span data-stu-id="d2f78-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f78-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2f78-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f78-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d2f78-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d2f78-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2f78-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f78-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d2f78-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2f78-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2f78-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2f78-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f78-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d2f78-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2f78-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2f78-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2f78-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2f78-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2f78-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2f78-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f78-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




