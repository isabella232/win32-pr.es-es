---
title: Propiedad nombre de ITsSbEnvironment
description: Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Propiedad Nombre Servicios de Escritorio remoto
- Propiedad Nombre Servicios de Escritorio remoto, interfaz ITsSbEnvironment
- Servicios de Escritorio remoto de la interfaz ITsSbEnvironment, propiedad Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996134"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="d3425-106">ITsSbEnvironment:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d3425-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="d3425-107">Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="d3425-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="d3425-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d3425-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3425-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3425-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="d3425-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d3425-110">Property value</span></span>

<span data-ttu-id="d3425-111">Un puntero a una variable **BSTR** que contiene el nombre del entorno.</span><span class="sxs-lookup"><span data-stu-id="d3425-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3425-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3425-112">Remarks</span></span>

<span data-ttu-id="d3425-113">Este método devuelve una cadena que no usa directamente Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="d3425-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="d3425-114">El agente de conexión a escritorio remoto pasa esta cadena a complementos de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3425-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3425-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3425-115">Requirements</span></span>



| <span data-ttu-id="d3425-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3425-116">Requirement</span></span> | <span data-ttu-id="d3425-117">Value</span><span class="sxs-lookup"><span data-stu-id="d3425-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3425-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3425-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d3425-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d3425-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d3425-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3425-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d3425-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d3425-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d3425-122">IDL</span><span class="sxs-lookup"><span data-stu-id="d3425-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3425-123"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3425-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3425-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3425-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3425-125">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d3425-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





