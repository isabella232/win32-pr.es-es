---
title: RPC_IF_HANDLE (Rpcdce. h)
description: El \_ tipo de datos RPC if \_ Handle declara un identificador de interfaz.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9590973d5ae1e82d89d6151e224b771d9f55ecc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996856"
---
# <a name="rpc_if_handle"></a><span data-ttu-id="cbabb-104">identificador de RPC \_ If \_</span><span class="sxs-lookup"><span data-stu-id="cbabb-104">RPC\_IF\_HANDLE</span></span>

<span data-ttu-id="cbabb-105">El tipo de datos **RPC \_ If \_ Handle** declara un identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="cbabb-105">The **RPC\_IF\_HANDLE** data type declares an interface handle.</span></span>


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="cbabb-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cbabb-106">Remarks</span></span>

<span data-ttu-id="cbabb-107">La biblioteca en tiempo de ejecución de RPC utiliza identificadores de interfaz para tener acceso a la estructura de datos de la especificación de interfaz.</span><span class="sxs-lookup"><span data-stu-id="cbabb-107">The RPC run-time library uses interface handles to access the interface-specification data structure.</span></span> <span data-ttu-id="cbabb-108">El compilador MIDL crea automáticamente una estructura de datos de especificación de interfaz a partir de cada archivo IDL y crea una variable global de tipo RPC \_ si es \_ el identificador de la especificación de interfaz.</span><span class="sxs-lookup"><span data-stu-id="cbabb-108">The MIDL compiler automatically creates an interface-specification data structure from each IDL file and creates a global variable of type RPC\_IF\_HANDLE for the interface specification.</span></span>

<span data-ttu-id="cbabb-109">El compilador MIDL incluye un identificador de interfaz en cada archivo de encabezado generado para la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cbabb-109">The MIDL compiler includes an interface handle in each header file generated for the interface.</span></span> <span data-ttu-id="cbabb-110">Las funciones que requieren la especificación de interfaz como parámetro muestran un tipo de datos de **RPC si es el \_ \_ identificador**.</span><span class="sxs-lookup"><span data-stu-id="cbabb-110">Functions requiring the interface specification as a parameter show a data type of **RPC\_IF\_HANDLE**.</span></span> <span data-ttu-id="cbabb-111">El formato de cada nombre de identificador de interfaz es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbabb-111">The form of each interface handle name is as follows:</span></span>

-   <span data-ttu-id="cbabb-112">*If-Name* \_ ClientIfHandle (para el cliente)</span><span class="sxs-lookup"><span data-stu-id="cbabb-112">*if-name*\_ClientIfHandle (for the client)</span></span>
-   <span data-ttu-id="cbabb-113">*If-Name* \_ ServerIfHandle (para el servidor)</span><span class="sxs-lookup"><span data-stu-id="cbabb-113">*if-name*\_ServerIfHandle (for the server)</span></span>

<span data-ttu-id="cbabb-114">La parte *If-Name* especifica el identificador de interfaz en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="cbabb-114">The *if-name* part specifies the interface identifier in the IDL file.</span></span>

<span data-ttu-id="cbabb-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cbabb-115">For example:</span></span>

<span data-ttu-id="cbabb-116">Hola \_ ClientIfHandle</span><span class="sxs-lookup"><span data-stu-id="cbabb-116">hello\_ClientIfHandle</span></span>

<span data-ttu-id="cbabb-117">Hola \_ ServerIfHandle</span><span class="sxs-lookup"><span data-stu-id="cbabb-117">hello\_ServerIfHandle</span></span>

> [!Note]  
> <span data-ttu-id="cbabb-118">La longitud máxima del nombre del identificador de interfaz es de 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbabb-118">The maximum length of the interface handle name is 31 characters.</span></span>

 

<span data-ttu-id="cbabb-119">Dado que las \_ partes "ClientIfHandle" y " \_ ServerIfHandle" de los nombres requieren 15 caracteres, el elemento *If-Name* no puede tener más de 16 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cbabb-119">Because the "\_ClientIfHandle" and "\_ServerIfHandle" parts of the names require 15 characters, the *if-name* element can be no more than 16 characters long.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbabb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbabb-120">Requirements</span></span>



| <span data-ttu-id="cbabb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbabb-121">Requirement</span></span> | <span data-ttu-id="cbabb-122">Value</span><span class="sxs-lookup"><span data-stu-id="cbabb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbabb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbabb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cbabb-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cbabb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cbabb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbabb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cbabb-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbabb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cbabb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbabb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbabb-128"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbabb-128"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





