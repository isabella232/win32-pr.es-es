---
description: Una solicitud para enviar rutas de acceso de símbolos de depuración al motor local (no remoto).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISymbolSettings:: UpdateSymbolSettings (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714679"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="5f921-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings:: UpdateSymbolSettings (método)</span><span class="sxs-lookup"><span data-stu-id="5f921-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="5f921-104">Una solicitud para enviar rutas de acceso de símbolos de depuración al motor local (no remoto).</span><span class="sxs-lookup"><span data-stu-id="5f921-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f921-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f921-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="5f921-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f921-106">Parameters</span></span>

<span data-ttu-id="5f921-107">*symbolServerInfo* </span><span class="sxs-lookup"><span data-stu-id="5f921-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="5f921-108">Información de ruta de acceso del servidor de símbolos de depuración</span><span class="sxs-lookup"><span data-stu-id="5f921-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f921-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f921-109">Return value</span></span>

<span data-ttu-id="5f921-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5f921-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f921-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f921-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f921-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f921-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5f921-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f921-113">Header</span></span></p></td><td><span data-ttu-id="5f921-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5f921-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5f921-115"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="5f921-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5f921-116">**ISymbolSettings**</span><span class="sxs-lookup"><span data-stu-id="5f921-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
