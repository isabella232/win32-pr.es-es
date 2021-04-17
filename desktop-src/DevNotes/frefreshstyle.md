---
description: Vuelve a cargar la configuración de color del registro.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660545"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="c9138-103">FRefreshStyle función)</span><span class="sxs-lookup"><span data-stu-id="c9138-103">FRefreshStyle function</span></span>

<span data-ttu-id="c9138-104">Vuelve a cargar la configuración de color del registro.</span><span class="sxs-lookup"><span data-stu-id="c9138-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9138-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9138-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="c9138-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9138-106">Parameters</span></span>

<span data-ttu-id="c9138-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c9138-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9138-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9138-108">Return value</span></span>

<span data-ttu-id="c9138-109">Devuelve TRUE si se ejecuta correctamente; en caso contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="c9138-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9138-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9138-110">Remarks</span></span>

<span data-ttu-id="c9138-111">Esta función no está asociada a una biblioteca de importación o un archivo de encabezado; se debe llamar mediante las funciones [**LoadLibrary**](-loadlibrary.md) y [**GetProcAddress**](-getprocaddress-.md) .</span><span class="sxs-lookup"><span data-stu-id="c9138-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9138-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9138-112">Requirements</span></span>



| <span data-ttu-id="c9138-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9138-113">Requirement</span></span> | <span data-ttu-id="c9138-114">Value</span><span class="sxs-lookup"><span data-stu-id="c9138-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9138-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9138-115">DLL</span></span><br/> | <dl> <span data-ttu-id="c9138-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9138-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9138-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9138-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9138-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c9138-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="c9138-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="c9138-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




