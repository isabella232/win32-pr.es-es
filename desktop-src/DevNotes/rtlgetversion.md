---
description: Obtiene la información de versión del sistema operativo que se está ejecutando actualmente.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Función RtlGetVersion (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152964"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="2fadf-103">RtlGetVersion función)</span><span class="sxs-lookup"><span data-stu-id="2fadf-103">RtlGetVersion function</span></span>

<span data-ttu-id="2fadf-104">Obtiene la información de versión del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="2fadf-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fadf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fadf-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="2fadf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fadf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fadf-107">*lpVersionInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2fadf-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fadf-108">Puntero a una estructura [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) o a una [**estructura \_ RTL OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) que contiene la información de versión del sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="2fadf-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="2fadf-109">Un llamador especifica la estructura de entrada que se utiliza estableciendo el miembro **dwOSVersionInfoSize** de la estructura en el tamaño en bytes de la estructura que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2fadf-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fadf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fadf-110">Return value</span></span>

<span data-ttu-id="2fadf-111">Devuelve el estado \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="2fadf-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fadf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fadf-112">Remarks</span></span>

<span data-ttu-id="2fadf-113">**RtlGetVersion** es el equivalente de la función [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2fadf-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="2fadf-114">Vea el ejemplo del Windows SDK que muestra cómo obtener la versión del sistema.</span><span class="sxs-lookup"><span data-stu-id="2fadf-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="2fadf-115">Al usar **RtlGetVersion** para determinar si se está ejecutando una versión determinada del sistema operativo, el autor de la llamada debe comprobar si los números de versión son mayores o iguales que el número de versión requerido.</span><span class="sxs-lookup"><span data-stu-id="2fadf-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="2fadf-116">Esto garantiza que una prueba de versión se realiza correctamente para las versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="2fadf-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="2fadf-117">Dado que las características del sistema operativo se pueden agregar en un archivo DLL redistribuible, comprobar solo los números de versión principal y secundaria no es la forma más confiable de comprobar la presencia de una característica específica del sistema.</span><span class="sxs-lookup"><span data-stu-id="2fadf-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="2fadf-118">Un controlador debe usar [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) para comprobar la presencia de una característica específica del sistema.</span><span class="sxs-lookup"><span data-stu-id="2fadf-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fadf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fadf-119">Requirements</span></span>



| <span data-ttu-id="2fadf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fadf-120">Requirement</span></span> | <span data-ttu-id="2fadf-121">Value</span><span class="sxs-lookup"><span data-stu-id="2fadf-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fadf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fadf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2fadf-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2fadf-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2fadf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fadf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2fadf-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2fadf-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2fadf-126">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="2fadf-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="2fadf-127"><dt>[Mundo](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="2fadf-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="2fadf-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fadf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fadf-129"><dt>Ntddk. h (incluye Ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fadf-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="2fadf-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fadf-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2fadf-131"><dt>Ntdll. lib; </dt> <dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fadf-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="2fadf-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fadf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fadf-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fadf-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fadf-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fadf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fadf-135">**PsGetVersion**</span><span class="sxs-lookup"><span data-stu-id="2fadf-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
