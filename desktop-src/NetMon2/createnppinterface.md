---
description: La función CreateNPPInterface usa el BLOB que devuelve el buscador para crear un NPP que la aplicación puede usar.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Función CreateNPPInterface (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002241"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="65142-103">CreateNPPInterface función)</span><span class="sxs-lookup"><span data-stu-id="65142-103">CreateNPPInterface function</span></span>

<span data-ttu-id="65142-104">La función **CreateNPPInterface** usa el BLOB que devuelve el buscador para crear un NPP que la aplicación puede usar.</span><span class="sxs-lookup"><span data-stu-id="65142-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="65142-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65142-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="65142-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65142-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65142-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65142-108">Identificador del BLOB que devuelve el buscador.</span><span class="sxs-lookup"><span data-stu-id="65142-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="65142-109">*IID* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="65142-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65142-110">Identificador de la interfaz a la que se llama desde NPP (**IRTC** o **IDelaydC**, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="65142-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="65142-111">*ppvObject* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65142-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65142-112">Puntero al puntero devuelto a la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="65142-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65142-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65142-113">Return value</span></span>

<span data-ttu-id="65142-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="65142-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="65142-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="65142-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="65142-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65142-116">Requirements</span></span>



| <span data-ttu-id="65142-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65142-117">Requirement</span></span> | <span data-ttu-id="65142-118">Value</span><span class="sxs-lookup"><span data-stu-id="65142-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65142-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65142-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65142-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="65142-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65142-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65142-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65142-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65142-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65142-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65142-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65142-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="65142-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="65142-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65142-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="65142-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65142-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="65142-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65142-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65142-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65142-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




