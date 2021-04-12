---
description: Devolución de llamada para devolver datos de la tabla de objetos.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IObjectTableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152680"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="ca2e5-103"><span id="vspixengine.iobjecttablecallback"></span>Interfaz IObjectTableCallback</span><span class="sxs-lookup"><span data-stu-id="ca2e5-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="ca2e5-104">Devolución de llamada para devolver datos de la tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="ca2e5-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca2e5-105">Members</span></span>

<span data-ttu-id="ca2e5-106">La interfaz **IObjectTableCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ca2e5-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ca2e5-107">**IObjectTableCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ca2e5-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ca2e5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ca2e5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ca2e5-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="ca2e5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ca2e5-110">La interfaz **IObjectTableCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ca2e5-111">Método</span><span class="sxs-lookup"><span data-stu-id="ca2e5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ca2e5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca2e5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ca2e5-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca2e5-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ca2e5-114">Obtiene información sobre qué columnas (tipos de datos de objeto) son compatibles con la tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ca2e5-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca2e5-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ca2e5-116">Función de devolución de llamada que se usa para notificar al host la información de la tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ca2e5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca2e5-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ca2e5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca2e5-118">Header</span></span></p></td><td><span data-ttu-id="ca2e5-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ca2e5-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
