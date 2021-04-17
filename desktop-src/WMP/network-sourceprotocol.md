---
title: Network. sourceProtocol
description: La propiedad sourceProtocol recupera el protocolo de origen usado para recibir los datos.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Windows Media Player de red. sourceProtocol
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699480"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="530b3-104">Network. sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="530b3-104">Network.sourceProtocol</span></span>

<span data-ttu-id="530b3-105">La propiedad **sourceProtocol** recupera el protocolo de origen usado para recibir los datos.</span><span class="sxs-lookup"><span data-stu-id="530b3-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="530b3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="530b3-106">Syntax</span></span>

<span data-ttu-id="530b3-107">*reproductor*. *red*. **sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="530b3-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="530b3-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="530b3-108">Possible Values</span></span>

<span data-ttu-id="530b3-109">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="530b3-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="530b3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="530b3-110">Remarks</span></span>

<span data-ttu-id="530b3-111">Esta propiedad se establece en "" (cadena vacía) al reproducir archivos multimedia desde un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="530b3-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="530b3-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="530b3-112">Examples</span></span>

<span data-ttu-id="530b3-113">En el siguiente ejemplo de JScript se usa *Network*. **sourceProtocol** para mostrar el protocolo de origen usado para recibir datos.</span><span class="sxs-lookup"><span data-stu-id="530b3-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="530b3-114">La información se muestra en un DIV HTML creado con ID = "SP".</span><span class="sxs-lookup"><span data-stu-id="530b3-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="530b3-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="530b3-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="530b3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="530b3-116">Requirements</span></span>



| <span data-ttu-id="530b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="530b3-117">Requirement</span></span> | <span data-ttu-id="530b3-118">Value</span><span class="sxs-lookup"><span data-stu-id="530b3-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="530b3-119">Versión</span><span class="sxs-lookup"><span data-stu-id="530b3-119">Version</span></span><br/> | <span data-ttu-id="530b3-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="530b3-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="530b3-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="530b3-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="530b3-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="530b3-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530b3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="530b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530b3-124">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="530b3-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





