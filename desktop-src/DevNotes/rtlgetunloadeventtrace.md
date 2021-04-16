---
description: Permite al código de volcado obtener la información de módulo descargada de Ntdll.dll para el almacenamiento en el minivolcado.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649999"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="4c86f-103">RtlGetUnloadEventTrace función)</span><span class="sxs-lookup"><span data-stu-id="4c86f-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="4c86f-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="4c86f-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="4c86f-105">Permite al código de volcado obtener la información de módulo descargada de Ntdll.dll para el almacenamiento en el minivolcado.</span><span class="sxs-lookup"><span data-stu-id="4c86f-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c86f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c86f-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="4c86f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c86f-107">Parameters</span></span>

<span data-ttu-id="4c86f-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4c86f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c86f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c86f-109">Return value</span></span>

<span data-ttu-id="4c86f-110">Esta función devuelve un puntero a una matriz.</span><span class="sxs-lookup"><span data-stu-id="4c86f-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="4c86f-111">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4c86f-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c86f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c86f-112">Remarks</span></span>

<span data-ttu-id="4c86f-113">La matriz RtlpUnloadEventTrace se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4c86f-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="4c86f-114">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="4c86f-114">This function has no associated header file.</span></span> <span data-ttu-id="4c86f-115">La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="4c86f-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="4c86f-116">También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4c86f-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c86f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c86f-117">Requirements</span></span>



| <span data-ttu-id="4c86f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c86f-118">Requirement</span></span> | <span data-ttu-id="4c86f-119">Value</span><span class="sxs-lookup"><span data-stu-id="4c86f-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c86f-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c86f-120">DLL</span></span><br/> | <dl> <span data-ttu-id="4c86f-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c86f-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
