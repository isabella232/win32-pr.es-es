---
description: Recupera los atributos básicos del objeto de archivo especificado.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670626"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="b35c5-103">NtQueryAttributesFile función)</span><span class="sxs-lookup"><span data-stu-id="b35c5-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="b35c5-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="b35c5-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="b35c5-105">Recupera los atributos básicos del objeto de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b35c5-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b35c5-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="b35c5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b35c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b35c5-108">*ObjectAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b35c5-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b35c5-109">Puntero a una estructura [de \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) que proporciona los atributos que se van a utilizar para el objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="b35c5-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="b35c5-110">*FileInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b35c5-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b35c5-111">Puntero a una estructura [de \_ \_ información básica de archivo](https://msdn.microsoft.com/library/aa491634.aspx) para recibir la información de atributo de archivo devuelta.</span><span class="sxs-lookup"><span data-stu-id="b35c5-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b35c5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b35c5-112">Return value</span></span>

<span data-ttu-id="b35c5-113">Devuelve un código de error NTSTATUS o.</span><span class="sxs-lookup"><span data-stu-id="b35c5-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="b35c5-114">Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.</span><span class="sxs-lookup"><span data-stu-id="b35c5-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b35c5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b35c5-115">Remarks</span></span>

<span data-ttu-id="b35c5-116">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="b35c5-116">This function has no associated header file.</span></span> <span data-ttu-id="b35c5-117">La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="b35c5-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="b35c5-118">También puede utilizar las funciones [**LoadLibrary**](-loadlibrary.md) y [**GetProcAddress**](-getprocaddress-.md) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="b35c5-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b35c5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b35c5-119">Requirements</span></span>



| <span data-ttu-id="b35c5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b35c5-120">Requirement</span></span> | <span data-ttu-id="b35c5-121">Value</span><span class="sxs-lookup"><span data-stu-id="b35c5-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b35c5-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b35c5-122">DLL</span></span><br/> | <dl> <span data-ttu-id="b35c5-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b35c5-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




