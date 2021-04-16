---
description: Cierra el administrador de OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649649"
---
# <a name="octerminate-function"></a><span data-ttu-id="2647a-103">OcTerminate función)</span><span class="sxs-lookup"><span data-stu-id="2647a-103">OcTerminate function</span></span>

<span data-ttu-id="2647a-104">Cierra el administrador de OC.</span><span class="sxs-lookup"><span data-stu-id="2647a-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="2647a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2647a-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="2647a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2647a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2647a-107">*OcManagerContext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2647a-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2647a-108">En la entrada, contiene el puntero de contexto del administrador de OC devuelto por [**OcInitialize**](ocinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="2647a-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="2647a-109">En la salida, recibe **null**.</span><span class="sxs-lookup"><span data-stu-id="2647a-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2647a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2647a-110">Return value</span></span>

<span data-ttu-id="2647a-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2647a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2647a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2647a-112">Remarks</span></span>

<span data-ttu-id="2647a-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2647a-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2647a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2647a-114">Requirements</span></span>



| <span data-ttu-id="2647a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2647a-115">Requirement</span></span> | <span data-ttu-id="2647a-116">Value</span><span class="sxs-lookup"><span data-stu-id="2647a-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2647a-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2647a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="2647a-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2647a-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2647a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2647a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2647a-120">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="2647a-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
