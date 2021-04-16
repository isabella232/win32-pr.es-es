---
description: Recupera el destino de un vínculo simbólico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649628"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="a7514-103">NtQuerySymbolicLinkObject función)</span><span class="sxs-lookup"><span data-stu-id="a7514-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="a7514-104">\[Esta función puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a7514-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a7514-105">Recupera el destino de un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="a7514-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7514-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7514-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="a7514-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7514-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7514-108">*LinkHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7514-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7514-109">Identificador del objeto de vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="a7514-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="a7514-110">*LinkTarget* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a7514-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7514-111">Puntero a una cadena Unicode inicializada que recibe el destino del vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="a7514-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="a7514-112">Se deben establecer los miembros **MaximumLength** y **buffer** si se produce un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="a7514-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="a7514-113">*ReturnedLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a7514-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7514-114">Puntero a una variable que recibe la longitud de la cadena Unicode devuelta en el parámetro *LinkTarget* .</span><span class="sxs-lookup"><span data-stu-id="a7514-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="a7514-115">Si la función devuelve **un \_ búfer de estado \_ demasiado \_ pequeño**, esta variable recibe el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="a7514-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7514-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7514-116">Return value</span></span>

<span data-ttu-id="a7514-117">La función devuelve el **estado \_ correcto** o un estado de error.</span><span class="sxs-lookup"><span data-stu-id="a7514-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7514-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7514-118">Remarks</span></span>

<span data-ttu-id="a7514-119">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a7514-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7514-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7514-120">Requirements</span></span>



| <span data-ttu-id="a7514-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7514-121">Requirement</span></span> | <span data-ttu-id="a7514-122">Value</span><span class="sxs-lookup"><span data-stu-id="a7514-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7514-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7514-123">DLL</span></span><br/> | <dl> <span data-ttu-id="a7514-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7514-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7514-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7514-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7514-126">**NtOpenSymbolicLinkObject**</span><span class="sxs-lookup"><span data-stu-id="a7514-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
