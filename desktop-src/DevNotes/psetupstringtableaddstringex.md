---
description: Agrega una cadena y datos adicionales a una tabla.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670672"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="3901a-103">pSetupStringTableAddStringEx función)</span><span class="sxs-lookup"><span data-stu-id="3901a-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="3901a-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="3901a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="3901a-105">Agrega una cadena y datos adicionales a una tabla.</span><span class="sxs-lookup"><span data-stu-id="3901a-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="3901a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3901a-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="3901a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3901a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3901a-108">*StringTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3901a-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3901a-109">Puntero a la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="3901a-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="3901a-110">*Cadena* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3901a-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3901a-111">Puntero a la cadena que se va a agregar a la tabla.</span><span class="sxs-lookup"><span data-stu-id="3901a-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="3901a-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3901a-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3901a-113">El valor de este parámetro puede ser `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="3901a-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="3901a-114">Value</span><span class="sxs-lookup"><span data-stu-id="3901a-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="3901a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="3901a-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="3901a-116"><dt>**STRTAB \_ 0x001 que \_ distingue mayúsculas de minúsculas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3901a-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="3901a-117">String distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3901a-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="3901a-118"><dt>**STRTAB \_ NEW \_ ExtraData**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="3901a-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="3901a-119">Hay datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="3901a-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="3901a-120">*ExtraData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3901a-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3901a-121">Un puntero opcional a un objeto de datos adicional.</span><span class="sxs-lookup"><span data-stu-id="3901a-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="3901a-122">*ExtraDataSize* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3901a-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3901a-123">Tamaño de los datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="3901a-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3901a-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3901a-124">Remarks</span></span>

<span data-ttu-id="3901a-125">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3901a-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3901a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3901a-126">Requirements</span></span>



| <span data-ttu-id="3901a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3901a-127">Requirement</span></span> | <span data-ttu-id="3901a-128">Value</span><span class="sxs-lookup"><span data-stu-id="3901a-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3901a-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3901a-129">DLL</span></span><br/> | <dl> <span data-ttu-id="3901a-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3901a-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
