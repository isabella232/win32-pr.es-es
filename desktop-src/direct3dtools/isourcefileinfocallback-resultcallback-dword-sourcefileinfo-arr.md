---
description: Función de devolución de llamada que se usa para notificar al host de información acerca de los archivos de código fuente asociados a la pila de llamadas.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISourceFileInfoCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152676"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="47914-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="47914-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="47914-104">Función de devolución de llamada que se usa para notificar al host de información acerca de los archivos de código fuente asociados a la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="47914-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="47914-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47914-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="47914-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47914-106">Parameters</span></span>

<span data-ttu-id="47914-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="47914-107">*count* </span></span>  
<span data-ttu-id="47914-108">Número de archivos de código fuente devueltos.</span><span class="sxs-lookup"><span data-stu-id="47914-108">The number of source files returned.</span></span>

<span data-ttu-id="47914-109">*count0 \_ sourceFileInfoBuffer* </span><span class="sxs-lookup"><span data-stu-id="47914-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="47914-110">Archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="47914-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="47914-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47914-111">Return value</span></span>

<span data-ttu-id="47914-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="47914-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="47914-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="47914-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="47914-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47914-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="47914-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47914-115">Header</span></span></p></td><td><span data-ttu-id="47914-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="47914-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="47914-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="47914-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="47914-118">**ISourceFileInfoCallback**</span><span class="sxs-lookup"><span data-stu-id="47914-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
