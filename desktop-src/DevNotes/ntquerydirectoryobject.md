---
description: Recupera información sobre el objeto de directorio especificado.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649629"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="9b376-103">NtQueryDirectoryObject función)</span><span class="sxs-lookup"><span data-stu-id="9b376-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="9b376-104">\[Esta función puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9b376-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9b376-105">Recupera información sobre el objeto de directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="9b376-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b376-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b376-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="9b376-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b376-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b376-108">*DirectoryHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b376-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-109">Identificador del objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="9b376-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-110">*Búfer* \[ de out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9b376-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-111">Un puntero a un búfer que recibe la información de directorio.</span><span class="sxs-lookup"><span data-stu-id="9b376-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="9b376-112">Este búfer recibe una o más estructuras de **\_ \_ información de directorio de objetos** , la última, que es **null**, y las cadenas que contienen los nombres de las entradas de directorio.</span><span class="sxs-lookup"><span data-stu-id="9b376-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="9b376-113">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="9b376-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-114">*Longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b376-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-115">Tamaño del búfer de salida proporcionado por el usuario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="9b376-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-116">*ReturnSingleEntry* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b376-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-117">Indica si la función debe devolver una sola entrada.</span><span class="sxs-lookup"><span data-stu-id="9b376-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-118">*RestartScan* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b376-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-119">Indica si se debe reiniciar el examen o continuar la enumeración con la información pasada en el parámetro de *contexto* .</span><span class="sxs-lookup"><span data-stu-id="9b376-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-120">*Contexto* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="9b376-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-121">Contexto de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="9b376-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="9b376-122">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9b376-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9b376-123">Puntero a una variable que recibe la longitud de la información de directorio devuelta en el búfer de salida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="9b376-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b376-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b376-124">Return value</span></span>

<span data-ttu-id="9b376-125">La función devuelve el **estado \_ correcto** o un estado de error.</span><span class="sxs-lookup"><span data-stu-id="9b376-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b376-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b376-126">Remarks</span></span>

<span data-ttu-id="9b376-127">La siguiente es la definición de la estructura de **\_ \_ información de directorio de objetos** .</span><span class="sxs-lookup"><span data-stu-id="9b376-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="9b376-128">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9b376-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b376-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b376-129">Requirements</span></span>



| <span data-ttu-id="9b376-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b376-130">Requirement</span></span> | <span data-ttu-id="9b376-131">Value</span><span class="sxs-lookup"><span data-stu-id="9b376-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b376-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b376-132">DLL</span></span><br/> | <dl> <span data-ttu-id="9b376-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b376-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b376-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b376-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b376-135">**NtOpenDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="9b376-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
