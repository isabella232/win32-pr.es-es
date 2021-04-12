---
title: Propiedad de entorno ITsSbClientConnection
description: Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedades de entorno
- Propiedad de entorno Servicios de Escritorio remoto, interfaz ITsSbClientConnection
- Servicios de Escritorio remoto de la interfaz ITsSbClientConnection, propiedad de entorno
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491615"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="4d528-106">ITsSbClientConnection:: Environment (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4d528-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="4d528-107">Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="4d528-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="4d528-108">Por ejemplo, en un escenario de escritorio virtual, este objeto contiene información sobre el equipo que hospeda la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4d528-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="4d528-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d528-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d528-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d528-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="4d528-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4d528-111">Property value</span></span>

<span data-ttu-id="4d528-112">Un puntero a un puntero a un objeto de entorno [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .</span><span class="sxs-lookup"><span data-stu-id="4d528-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d528-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4d528-113">Error codes</span></span>

<span data-ttu-id="4d528-114">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4d528-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d528-115">De lo contrario, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="4d528-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4d528-116">Los valores posibles incluyen, entre otros, los que aparecen en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d528-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4d528-117">\_puntero E</span><span class="sxs-lookup"><span data-stu-id="4d528-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="4d528-118">No se encontró el entorno.</span><span class="sxs-lookup"><span data-stu-id="4d528-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d528-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d528-119">Remarks</span></span>

<span data-ttu-id="4d528-120">Un complemento de orquestación puede llamar a este método para recuperar información de entorno sobre una máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="4d528-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d528-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d528-121">Requirements</span></span>



| <span data-ttu-id="4d528-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d528-122">Requirement</span></span> | <span data-ttu-id="4d528-123">Value</span><span class="sxs-lookup"><span data-stu-id="4d528-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4d528-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d528-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d528-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d528-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4d528-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d528-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d528-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d528-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="4d528-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4d528-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d528-129"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d528-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d528-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d528-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d528-131">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="4d528-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





