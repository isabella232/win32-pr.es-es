---
description: Abre un vínculo simbólico existente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671023"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="00d2d-103">NtOpenSymbolicLinkObject función)</span><span class="sxs-lookup"><span data-stu-id="00d2d-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="00d2d-104">\[Esta función puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="00d2d-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="00d2d-105">Abre un vínculo simbólico existente.</span><span class="sxs-lookup"><span data-stu-id="00d2d-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00d2d-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="00d2d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00d2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d2d-108">*LinkHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="00d2d-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d2d-109">Identificador del objeto de vínculo simbólico recién abierto.</span><span class="sxs-lookup"><span data-stu-id="00d2d-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="00d2d-110">*DesiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00d2d-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d2d-111">Una [**\_ máscara de acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="00d2d-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="00d2d-112">Es habitual utilizar \_ la lectura genérica para que el identificador se pueda pasar a la función [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .</span><span class="sxs-lookup"><span data-stu-id="00d2d-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="00d2d-113">*ObjectAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="00d2d-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d2d-114">Atributos del objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="00d2d-114">The attributes for the directory object.</span></span> <span data-ttu-id="00d2d-115">Para inicializar la estructura de **\_ atributos de objeto** , use la macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="00d2d-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="00d2d-116">Si el llamador no se está ejecutando en un contexto de subproceso del sistema, debe especificar la marca de **\_ \_ identificador de kernel de obj** al inicializar la estructura.</span><span class="sxs-lookup"><span data-stu-id="00d2d-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="00d2d-117">Para obtener más información, consulte la documentación de estos elementos en la documentación del WDK.</span><span class="sxs-lookup"><span data-stu-id="00d2d-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d2d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00d2d-118">Return value</span></span>

<span data-ttu-id="00d2d-119">La función devuelve el **estado \_ correcto** o un estado de error.</span><span class="sxs-lookup"><span data-stu-id="00d2d-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d2d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00d2d-120">Remarks</span></span>

<span data-ttu-id="00d2d-121">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="00d2d-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d2d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d2d-122">Requirements</span></span>



| <span data-ttu-id="00d2d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d2d-123">Requirement</span></span> | <span data-ttu-id="00d2d-124">Value</span><span class="sxs-lookup"><span data-stu-id="00d2d-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00d2d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00d2d-125">DLL</span></span><br/> | <dl> <span data-ttu-id="00d2d-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d2d-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d2d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="00d2d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d2d-128">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="00d2d-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
