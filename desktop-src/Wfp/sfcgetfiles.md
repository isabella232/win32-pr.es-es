---
description: Enumera los archivos protegidos.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Función SfcGetFiles (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910594"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="8f26b-103">SfcGetFiles función)</span><span class="sxs-lookup"><span data-stu-id="8f26b-103">SfcGetFiles function</span></span>

<span data-ttu-id="8f26b-104">\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8f26b-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f26b-105">Se ha quitado la compatibilidad con esta función en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8f26b-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8f26b-106">En su lugar, use las funciones admitidas que se enumeran en [las funciones de WRP](wfp-functions.md) .\]</span><span class="sxs-lookup"><span data-stu-id="8f26b-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="8f26b-107">Enumera los archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="8f26b-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f26b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f26b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="8f26b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f26b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f26b-110">*ProtFileData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f26b-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f26b-111">Puntero a una estructura [**de \_ \_ entrada de archivo PPROTECT**](pprotect-file-entry.md) que contiene la lista de archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="8f26b-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="8f26b-112">*FileCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f26b-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f26b-113">Puntero a una ubicación que contiene un valor ULONG que es el número de archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="8f26b-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f26b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f26b-114">Return value</span></span>

<span data-ttu-id="8f26b-115">Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8f26b-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="8f26b-116">Si se produce un error en la función, devuelve el código de error NTSTATUS adecuado.</span><span class="sxs-lookup"><span data-stu-id="8f26b-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f26b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f26b-117">Requirements</span></span>



| <span data-ttu-id="8f26b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f26b-118">Requirement</span></span> | <span data-ttu-id="8f26b-119">Value</span><span class="sxs-lookup"><span data-stu-id="8f26b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f26b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f26b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f26b-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8f26b-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8f26b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f26b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f26b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f26b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f26b-124">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8f26b-124">End of client support</span></span><br/>    | <span data-ttu-id="8f26b-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f26b-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8f26b-126">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8f26b-126">End of server support</span></span><br/>    | <span data-ttu-id="8f26b-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f26b-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8f26b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f26b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f26b-129"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f26b-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f26b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f26b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f26b-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f26b-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f26b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f26b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f26b-133">**\_entrada de archivo PPROTECT \_**</span><span class="sxs-lookup"><span data-stu-id="8f26b-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




