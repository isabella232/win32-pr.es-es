---
description: Recupera el tipo MAC de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Función GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540203"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="b87ff-103">GetNPPMacTypeAsNumber función)</span><span class="sxs-lookup"><span data-stu-id="b87ff-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="b87ff-104">La función **GetNPPMacTypeAsNumber** recupera el tipo Mac de la categoría NetworkInfo de la sección NPP del BLOB y convierte los datos de tipo en un número de tipo Mac.</span><span class="sxs-lookup"><span data-stu-id="b87ff-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b87ff-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="b87ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b87ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87ff-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b87ff-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b87ff-108">Identificador del BLOB especificado.</span><span class="sxs-lookup"><span data-stu-id="b87ff-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b87ff-109">*lpMacType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b87ff-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b87ff-110">Un puntero al tipo MAC.</span><span class="sxs-lookup"><span data-stu-id="b87ff-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87ff-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b87ff-111">Return value</span></span>

<span data-ttu-id="b87ff-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b87ff-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b87ff-113">Si la etiqueta no está disponible, el valor devuelto es de \_ tipo Mac \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="b87ff-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="b87ff-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b87ff-114">Remarks</span></span>

<span data-ttu-id="b87ff-115">Esta función asigna la etiqueta, **NPP: NetworkInfo: MacType** al **\_ \_ \* tipo Mac** tal y como se define en el archivo Npptypes. h.</span><span class="sxs-lookup"><span data-stu-id="b87ff-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87ff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b87ff-116">Requirements</span></span>



| <span data-ttu-id="b87ff-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b87ff-117">Requirement</span></span> | <span data-ttu-id="b87ff-118">Value</span><span class="sxs-lookup"><span data-stu-id="b87ff-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b87ff-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b87ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b87ff-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b87ff-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b87ff-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b87ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b87ff-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b87ff-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b87ff-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b87ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b87ff-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b87ff-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b87ff-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b87ff-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="b87ff-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b87ff-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b87ff-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b87ff-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b87ff-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b87ff-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




