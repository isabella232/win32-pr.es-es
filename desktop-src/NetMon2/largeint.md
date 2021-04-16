---
description: El tipo de LARGEINT define un \_ valor entero grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677017"
---
# <a name="largeint"></a><span data-ttu-id="1534c-103">LARGEINT</span><span class="sxs-lookup"><span data-stu-id="1534c-103">LARGEINT</span></span>

<span data-ttu-id="1534c-104">El tipo de **LARGEINT** define un [**valor \_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .</span><span class="sxs-lookup"><span data-stu-id="1534c-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="1534c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1534c-105">Remarks</span></span>

<span data-ttu-id="1534c-106">El miembro **lpLargeIntTable** de la estructura de [**conjunto**](set.md) apunta a una matriz de estructuras **set** que definen uno o más valores de LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="1534c-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="1534c-107">Cuando se especifica este tipo de estructura de **conjunto** , monitor de red muestra una de las siguientes etiquetas con cada valor de LARGEINT que encuentra en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="1534c-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="1534c-108">Coincide con el valor establecido.</span><span class="sxs-lookup"><span data-stu-id="1534c-108">Matches set value.</span></span> <span data-ttu-id="1534c-109">El valor LARGEINT se incluye en el conjunto.</span><span class="sxs-lookup"><span data-stu-id="1534c-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="1534c-110">Valor establecido desconocido.</span><span class="sxs-lookup"><span data-stu-id="1534c-110">Unknown set value.</span></span> <span data-ttu-id="1534c-111">El valor LARGEINT no se incluye en el conjunto.</span><span class="sxs-lookup"><span data-stu-id="1534c-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1534c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1534c-112">Requirements</span></span>



| <span data-ttu-id="1534c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1534c-113">Requirement</span></span> | <span data-ttu-id="1534c-114">Value</span><span class="sxs-lookup"><span data-stu-id="1534c-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1534c-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1534c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1534c-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1534c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1534c-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1534c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1534c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1534c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1534c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1534c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1534c-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1534c-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1534c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1534c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1534c-122">SET</span><span class="sxs-lookup"><span data-stu-id="1534c-122">SET</span></span>](set.md)
</dt> </dl>

 

