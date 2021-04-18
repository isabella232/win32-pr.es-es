---
title: Propiedad de dominio ITsSbClientConnection
description: Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad de dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz ITsSbClientConnection
- Servicios de Escritorio remoto de la interfaz ITsSbClientConnection, propiedad del dominio
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686170"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="a9252-106">ITsSbClientConnection::D propiedad omain</span><span class="sxs-lookup"><span data-stu-id="a9252-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="a9252-107">Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="a9252-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="a9252-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a9252-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9252-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9252-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="a9252-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a9252-110">Property value</span></span>

<span data-ttu-id="a9252-111">Un puntero a una variable **BSTR** que contiene el nombre de dominio del cliente RDC.</span><span class="sxs-lookup"><span data-stu-id="a9252-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="a9252-112">Cuando haya terminado de usar la cadena, puede liberarla llamando a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="a9252-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9252-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9252-113">Requirements</span></span>



| <span data-ttu-id="a9252-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9252-114">Requirement</span></span> | <span data-ttu-id="a9252-115">Value</span><span class="sxs-lookup"><span data-stu-id="a9252-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9252-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9252-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9252-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a9252-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a9252-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9252-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9252-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9252-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a9252-120">IDL</span><span class="sxs-lookup"><span data-stu-id="a9252-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9252-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9252-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9252-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9252-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9252-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a9252-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

