---
description: Recupera el tamaño y la ubicación de la lista de módulos descargados dinámicamente para el proceso actual.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671361"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="57e6b-103">RtlGetUnloadEventTraceEx función)</span><span class="sxs-lookup"><span data-stu-id="57e6b-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="57e6b-104">Recupera el tamaño y la ubicación de la lista de módulos descargados dinámicamente para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="57e6b-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e6b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57e6b-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="57e6b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e6b-107">*Elementos de elemento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57e6b-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57e6b-108">Puntero a una variable que contiene el tamaño de un elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="57e6b-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="57e6b-109">*ElementCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57e6b-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57e6b-110">Puntero a una variable que contiene el número de elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="57e6b-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="57e6b-111">*Eventtracer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="57e6b-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57e6b-112">Puntero a una matriz de estructuras **de \_ \_ \_ seguimiento de eventos de la descarga RTL** .</span><span class="sxs-lookup"><span data-stu-id="57e6b-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="57e6b-113">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="57e6b-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e6b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57e6b-114">Return value</span></span>

<span data-ttu-id="57e6b-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="57e6b-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57e6b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57e6b-116">Remarks</span></span>

<span data-ttu-id="57e6b-117">El cargador almacena la información de eventos descargados en ubicaciones que se pueden leer en los procesos aprovechando el hecho de que Ntdll.dll se carga en la misma dirección base en todos los procesos.</span><span class="sxs-lookup"><span data-stu-id="57e6b-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="57e6b-118">Cuando un depurador necesita consultar información de módulo descargada, llama a esta función para determinar la dirección en la que residen las variables y, a continuación, consulta la memoria virtual en el proceso de destino en esas direcciones para leer los valores reales.</span><span class="sxs-lookup"><span data-stu-id="57e6b-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="57e6b-119">Cada elemento de la lista se define de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="57e6b-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="57e6b-120">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="57e6b-120">This function has no associated header file.</span></span> <span data-ttu-id="57e6b-121">La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="57e6b-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="57e6b-122">También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="57e6b-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="57e6b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57e6b-123">Requirements</span></span>



| <span data-ttu-id="57e6b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57e6b-124">Requirement</span></span> | <span data-ttu-id="57e6b-125">Value</span><span class="sxs-lookup"><span data-stu-id="57e6b-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57e6b-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57e6b-126">DLL</span></span><br/> | <dl> <span data-ttu-id="57e6b-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57e6b-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
