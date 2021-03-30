---
description: Devolución de llamada para devolver información del archivo de código fuente desde una pila de llamadas.
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz ISourceFileInfoCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806836"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="4f55c-103"><span id="vspixengine.isourcefileinfocallback"></span>Interfaz ISourceFileInfoCallback</span><span class="sxs-lookup"><span data-stu-id="4f55c-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="4f55c-104">Devolución de llamada para devolver información del archivo de código fuente desde una pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4f55c-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="4f55c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f55c-105">Members</span></span>

<span data-ttu-id="4f55c-106">La interfaz **ISourceFileInfoCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4f55c-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f55c-107">**ISourceFileInfoCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f55c-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4f55c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f55c-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4f55c-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="4f55c-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4f55c-110">La interfaz **ISourceFileInfoCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4f55c-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4f55c-111">Método</span><span class="sxs-lookup"><span data-stu-id="4f55c-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4f55c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f55c-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4f55c-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f55c-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4f55c-114">Función de devolución de llamada que se usa para notificar al host de información acerca de los archivos de código fuente asociados a la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4f55c-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4f55c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f55c-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4f55c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f55c-116">Header</span></span></p></td><td><span data-ttu-id="4f55c-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4f55c-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
