---
description: Identificador de un búfer de cadena mutable que se puede usar para crear un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696412"
---
# <a name="hstring_buffer"></a><span data-ttu-id="c49dc-103">\_búfer HSTRING</span><span class="sxs-lookup"><span data-stu-id="c49dc-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="c49dc-104">Identificador de un búfer de cadena mutable que se puede usar para crear un [**HSTRING**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="c49dc-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="c49dc-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c49dc-105">Remarks</span></span>

<span data-ttu-id="c49dc-106">**HSTRING \_ BUFFER** representa un búfer de cadena que se puede modificar antes de convertirlo en un [**HSTRING**](hstring.md)inmutable.</span><span class="sxs-lookup"><span data-stu-id="c49dc-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="c49dc-107">Llame a la función [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para crear **un \_ búfer de HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="c49dc-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="c49dc-108">Llame a [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para convertir un **\_ búfer de HSTRING** en un [**HSTRING**](hstring.md)inmutable.</span><span class="sxs-lookup"><span data-stu-id="c49dc-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c49dc-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c49dc-109">Requirements</span></span>



| <span data-ttu-id="c49dc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c49dc-110">Requirement</span></span> | <span data-ttu-id="c49dc-111">Value</span><span class="sxs-lookup"><span data-stu-id="c49dc-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c49dc-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c49dc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c49dc-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c49dc-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="c49dc-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c49dc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c49dc-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c49dc-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c49dc-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c49dc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c49dc-117"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="c49dc-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c49dc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c49dc-118">See also</span></span>

<dl> <span data-ttu-id="c49dc-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c49dc-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c49dc-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="c49dc-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="c49dc-121">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="c49dc-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="c49dc-122">**WindowsPromoteStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="c49dc-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
