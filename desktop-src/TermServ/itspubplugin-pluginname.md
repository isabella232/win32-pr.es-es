---
title: Propiedad pluginName de ItsPubPlugin
description: Recupera el nombre del complemento.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad pluginName
- propiedad pluginName Servicios de Escritorio remoto, interfaz ItsPubPlugin
- Servicios de Escritorio remoto de la interfaz ItsPubPlugin, propiedad pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686060"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="c5635-106">ItsPubPlugin::p propiedad luginName</span><span class="sxs-lookup"><span data-stu-id="c5635-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="c5635-107">Recupera el nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="c5635-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="c5635-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c5635-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5635-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5635-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c5635-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5635-110">Property value</span></span>

<span data-ttu-id="c5635-111">Un puntero a una variable **BSTR** para recibir el nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="c5635-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5635-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5635-112">Requirements</span></span>



| <span data-ttu-id="c5635-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5635-113">Requirement</span></span> | <span data-ttu-id="c5635-114">Value</span><span class="sxs-lookup"><span data-stu-id="c5635-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5635-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5635-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5635-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c5635-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c5635-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5635-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5635-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5635-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="c5635-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c5635-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5635-120"><dt>Cpubplugin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5635-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5635-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5635-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5635-122">**ItsPubPlugin**</span><span class="sxs-lookup"><span data-stu-id="c5635-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





