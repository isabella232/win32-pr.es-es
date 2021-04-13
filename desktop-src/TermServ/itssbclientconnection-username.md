---
title: Propiedad de nombre de usuario ITsSbClientConnection
description: Recupera un valor que indica el nombre del usuario que inició la conexión.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Propiedad UserName Servicios de Escritorio remoto
- Propiedad UserName Servicios de Escritorio remoto, interfaz ITsSbClientConnection
- Servicios de Escritorio remoto de la interfaz ITsSbClientConnection, propiedad UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359827"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="ac828-106">ITsSbClientConnection:: UserName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ac828-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="ac828-107">Recupera un valor que indica el nombre del usuario que inició la conexión.</span><span class="sxs-lookup"><span data-stu-id="ac828-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="ac828-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac828-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac828-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac828-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="ac828-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ac828-110">Property value</span></span>

<span data-ttu-id="ac828-111">Un puntero a un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="ac828-111">A pointer to a user name.</span></span> <span data-ttu-id="ac828-112">Cuando haya terminado de usar la cadena, puede liberarla llamando a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="ac828-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac828-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac828-113">Requirements</span></span>



| <span data-ttu-id="ac828-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac828-114">Requirement</span></span> | <span data-ttu-id="ac828-115">Value</span><span class="sxs-lookup"><span data-stu-id="ac828-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac828-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac828-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ac828-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac828-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ac828-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac828-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ac828-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac828-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="ac828-120">IDL</span><span class="sxs-lookup"><span data-stu-id="ac828-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac828-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac828-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac828-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac828-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac828-123">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="ac828-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

