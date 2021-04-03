---
description: Estructura que identifica el host y el archivo de código fuente que se va a evaluar.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION estructura (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080105"
---
# <a name="wldp_host_information-structure"></a><span data-ttu-id="953e9-103">Estructura de información de \_ host de WLDP \_</span><span class="sxs-lookup"><span data-stu-id="953e9-103">WLDP\_HOST\_INFORMATION structure</span></span>

<span data-ttu-id="953e9-104">Estructura que identifica el host y el archivo de código fuente que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="953e9-104">A structure identifying the host and source file to be evaluated.</span></span>

## <a name="syntax"></a><span data-ttu-id="953e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="953e9-105">Syntax</span></span>


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="953e9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="953e9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="953e9-107">**dwRevision**</span><span class="sxs-lookup"><span data-stu-id="953e9-107">**dwRevision**</span></span>
</dt> <dd>

<span data-ttu-id="953e9-108">Debe ser **la \_ \_ \_ revisión de información del host de WLDP**.</span><span class="sxs-lookup"><span data-stu-id="953e9-108">Must be **WLDP\_HOST\_INFORMATION\_REVISION**.</span></span>

</dd> <dt>

<span data-ttu-id="953e9-109">**dwHostId**</span><span class="sxs-lookup"><span data-stu-id="953e9-109">**dwHostId**</span></span>
</dt> <dd>

<span data-ttu-id="953e9-110">Valor de enumeración del [**\_ \_ ID**](wldp-host-id.md) . de host de WLDP que describe el identificador de host.</span><span class="sxs-lookup"><span data-stu-id="953e9-110">Enumeration value from [**WLDP\_HOST\_ID**](wldp-host-id.md) that describes the host ID.</span></span>

</dd> <dt>

<span data-ttu-id="953e9-111">**szSource**</span><span class="sxs-lookup"><span data-stu-id="953e9-111">**szSource**</span></span>
</dt> <dd>

<span data-ttu-id="953e9-112">Ruta de acceso completa y nombre de script con la extensión.</span><span class="sxs-lookup"><span data-stu-id="953e9-112">Full path and script name with the extension.</span></span> <span data-ttu-id="953e9-113">NULL para el ID. de **host de WLDP \_ \_ \_ global** o la ejecución de script manual.</span><span class="sxs-lookup"><span data-stu-id="953e9-113">NULL for **WLDP\_HOST\_ID\_GLOBAL**, or manual script execution.</span></span>

</dd> <dt>

<span data-ttu-id="953e9-114">**hSource**</span><span class="sxs-lookup"><span data-stu-id="953e9-114">**hSource**</span></span>
</dt> <dd>

<span data-ttu-id="953e9-115">Además del nombre, el llamador puede especificar un identificador para el archivo que se utiliza para la validación.</span><span class="sxs-lookup"><span data-stu-id="953e9-115">In addition to the name, the caller can specify a handle to the file used for validation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="953e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="953e9-116">Requirements</span></span>



| <span data-ttu-id="953e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="953e9-117">Requirement</span></span> | <span data-ttu-id="953e9-118">Value</span><span class="sxs-lookup"><span data-stu-id="953e9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="953e9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="953e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="953e9-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="953e9-120">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="953e9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="953e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="953e9-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="953e9-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="953e9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="953e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="953e9-124"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="953e9-124"><dt>Wldp.h</dt></span></span> </dl> |



 

 




