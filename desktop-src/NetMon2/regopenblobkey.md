---
description: La función RegOpenBlobKey recupera un BLOB almacenado en la clave del registro especificada.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Función RegOpenBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678513"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="bc21b-103">RegOpenBlobKey función)</span><span class="sxs-lookup"><span data-stu-id="bc21b-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="bc21b-104">La función **RegOpenBlobKey** recupera un BLOB almacenado en la clave del registro especificada.</span><span class="sxs-lookup"><span data-stu-id="bc21b-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc21b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc21b-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="bc21b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc21b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc21b-107">*HKEY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc21b-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc21b-108">Identificador de la clave del registro que contiene el BLOB.</span><span class="sxs-lookup"><span data-stu-id="bc21b-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="bc21b-109">*szBlobName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc21b-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc21b-110">Nombre que identifica el BLOB especificado en el registro.</span><span class="sxs-lookup"><span data-stu-id="bc21b-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="bc21b-111">*phBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc21b-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc21b-112">Puntero al BLOB que se recupera.</span><span class="sxs-lookup"><span data-stu-id="bc21b-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc21b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc21b-113">Return value</span></span>

<span data-ttu-id="bc21b-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bc21b-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bc21b-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="bc21b-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc21b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc21b-116">Requirements</span></span>



| <span data-ttu-id="bc21b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc21b-117">Requirement</span></span> | <span data-ttu-id="bc21b-118">Value</span><span class="sxs-lookup"><span data-stu-id="bc21b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc21b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc21b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bc21b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc21b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc21b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc21b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bc21b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc21b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc21b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc21b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc21b-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc21b-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bc21b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc21b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc21b-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc21b-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc21b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc21b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc21b-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc21b-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc21b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc21b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc21b-130">RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="bc21b-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




