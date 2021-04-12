---
title: Tipos de datos de DNS (windns. h)
ms.assetid: 652012a5-e45d-4ea6-896a-17e8b1ed4a05
description: 'Más información acerca de: tipos de datos DNS'
keywords:
- IP4_ADDRESS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2caa113670a749029b70df9772d6e2707684b7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276845"
---
# <a name="dns-data-types"></a><span data-ttu-id="25fc6-104">Tipos de datos de DNS</span><span class="sxs-lookup"><span data-stu-id="25fc6-104">DNS Data Types</span></span>

<span data-ttu-id="25fc6-105">Los siguientes tipos de datos se definen para DNS:</span><span class="sxs-lookup"><span data-stu-id="25fc6-105">The following data types are defined for DNS:</span></span>


```C++
typedef DWORD IP4_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="25fc6-106">**Dirección de IP4 \_**</span><span class="sxs-lookup"><span data-stu-id="25fc6-106">**IP4\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="25fc6-107">Valor que representa una dirección del Protocolo de Internet versión 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="25fc6-107">A value that represents an Internet Protocol version 4 (IPv4) address.</span></span> <span data-ttu-id="25fc6-108">Por ejemplo, la dirección IPv4 decimal con puntos, **127.0.0.1**, se representa en el orden de bytes del host como **0x7F000001**.</span><span class="sxs-lookup"><span data-stu-id="25fc6-108">For example, the dotted decimal IPv4 address, **127.0.0.1**, is represented in host byte order as **0x7F000001**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25fc6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25fc6-109">Requirements</span></span>



| <span data-ttu-id="25fc6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="25fc6-110">Requirement</span></span> | <span data-ttu-id="25fc6-111">Value</span><span class="sxs-lookup"><span data-stu-id="25fc6-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25fc6-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25fc6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="25fc6-113">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="25fc6-113">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="25fc6-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25fc6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="25fc6-115">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="25fc6-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25fc6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25fc6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="25fc6-117"><dt>Viento. h</dt></span><span class="sxs-lookup"><span data-stu-id="25fc6-117"><dt>Windns.h</dt></span></span> </dl> |



 

 





