---
description: El método GetMaximumCursors recupera el número máximo de cursores que admite un dispositivo de tableta gráfica.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3:: GetMaximumCursors (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720584"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="16953-103">ITablet3:: GetMaximumCursors (método)</span><span class="sxs-lookup"><span data-stu-id="16953-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="16953-104">El método **GetMaximumCursors** recupera el número máximo de cursores que admite un dispositivo de tableta gráfica.</span><span class="sxs-lookup"><span data-stu-id="16953-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="16953-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16953-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="16953-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="16953-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16953-107">*pMaximumCursors*</span><span class="sxs-lookup"><span data-stu-id="16953-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="16953-108">Número máximo de entradas que admite el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16953-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16953-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="16953-109">Return value</span></span>

<span data-ttu-id="16953-110">Devuelve \_ si es correcto; de lo contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="16953-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16953-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16953-111">Requirements</span></span>



| <span data-ttu-id="16953-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="16953-112">Requirement</span></span> | <span data-ttu-id="16953-113">Value</span><span class="sxs-lookup"><span data-stu-id="16953-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16953-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16953-114">Minimum supported client</span></span><br/> | <span data-ttu-id="16953-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="16953-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="16953-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16953-116">Minimum supported server</span></span><br/> | <span data-ttu-id="16953-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="16953-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="16953-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16953-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="16953-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16953-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16953-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="16953-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16953-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="16953-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




