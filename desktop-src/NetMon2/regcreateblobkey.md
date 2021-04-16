---
description: La función RegCreateBlobKey almacena un BLOB en la clave del registro especificada.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Función RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678514"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="ab935-103">RegCreateBlobKey función)</span><span class="sxs-lookup"><span data-stu-id="ab935-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="ab935-104">La función **RegCreateBlobKey** almacena un BLOB en la clave del registro especificada.</span><span class="sxs-lookup"><span data-stu-id="ab935-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab935-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab935-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="ab935-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab935-107">*HKEY* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab935-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab935-108">Identificador de la clave del registro donde se almacenará el BLOB.</span><span class="sxs-lookup"><span data-stu-id="ab935-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="ab935-109">*szBlobName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab935-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab935-110">Nombre (definido por la aplicación) que representa el BLOB en el registro.</span><span class="sxs-lookup"><span data-stu-id="ab935-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="ab935-111">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab935-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab935-112">Identificador del BLOB que se guarda.</span><span class="sxs-lookup"><span data-stu-id="ab935-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab935-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab935-113">Return value</span></span>

<span data-ttu-id="ab935-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ab935-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ab935-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="ab935-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab935-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab935-116">Requirements</span></span>



| <span data-ttu-id="ab935-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab935-117">Requirement</span></span> | <span data-ttu-id="ab935-118">Value</span><span class="sxs-lookup"><span data-stu-id="ab935-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab935-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab935-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab935-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab935-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ab935-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab935-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab935-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab935-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab935-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab935-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab935-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab935-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ab935-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab935-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab935-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab935-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab935-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab935-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab935-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab935-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab935-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab935-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab935-130">RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="ab935-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




