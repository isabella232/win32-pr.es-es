---
description: Determina si los componentes marcados en las opciones están instalados en el sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661019"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="f6285-103">IcfgNeedInetComponents función)</span><span class="sxs-lookup"><span data-stu-id="f6285-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="f6285-104">Determina si los componentes marcados en las opciones están instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f6285-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6285-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6285-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="f6285-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6285-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6285-107">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="f6285-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="f6285-108">Una combinación de las marcas siguientes que especifican qué componentes se deben detectar de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="f6285-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="f6285-109">Value</span><span class="sxs-lookup"><span data-stu-id="f6285-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="f6285-110">Significado</span><span class="sxs-lookup"><span data-stu-id="f6285-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="f6285-111"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f6285-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="f6285-112">¿Es necesario Exchange o Internet Mail?</span><span class="sxs-lookup"><span data-stu-id="f6285-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="f6285-113"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f6285-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="f6285-114">¿Es necesario RAS?</span><span class="sxs-lookup"><span data-stu-id="f6285-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="f6285-115"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f6285-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="f6285-116">¿Es necesario TCP/IP?</span><span class="sxs-lookup"><span data-stu-id="f6285-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="f6285-117">*lpfNeedComponents*</span><span class="sxs-lookup"><span data-stu-id="f6285-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="f6285-118">Si este valor no es **null**, es **true** en la devolución si uno o más componentes no están instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f6285-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6285-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6285-119">Return value</span></span>

<span data-ttu-id="f6285-120">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6285-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f6285-121">Si no se produce ningún error, devuelve el código de **error \_ correcto** .</span><span class="sxs-lookup"><span data-stu-id="f6285-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6285-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6285-122">Remarks</span></span>

<span data-ttu-id="f6285-123">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f6285-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6285-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6285-124">Requirements</span></span>



| <span data-ttu-id="f6285-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6285-125">Requirement</span></span> | <span data-ttu-id="f6285-126">Value</span><span class="sxs-lookup"><span data-stu-id="f6285-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6285-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6285-127">DLL</span></span><br/> | <dl> <span data-ttu-id="f6285-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6285-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
