---
description: Instala los componentes del sistema especificados.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649787"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="04a23-103">IcfgInstallInetComponents función)</span><span class="sxs-lookup"><span data-stu-id="04a23-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="04a23-104">Instala los componentes del sistema especificados.</span><span class="sxs-lookup"><span data-stu-id="04a23-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a23-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04a23-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="04a23-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04a23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a23-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="04a23-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="04a23-108">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="04a23-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="04a23-109">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="04a23-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="04a23-110">Combinación de las marcas siguientes que controlan la instalación y la configuración.</span><span class="sxs-lookup"><span data-stu-id="04a23-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="04a23-111">Value</span><span class="sxs-lookup"><span data-stu-id="04a23-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="04a23-112">Significado</span><span class="sxs-lookup"><span data-stu-id="04a23-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="04a23-113"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="04a23-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="04a23-114">Instale Exchange y correo de Internet.</span><span class="sxs-lookup"><span data-stu-id="04a23-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="04a23-115"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="04a23-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="04a23-116">Instalar RAS (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="04a23-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="04a23-117"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="04a23-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="04a23-118">Instale TCP/IP (si es necesario).</span><span class="sxs-lookup"><span data-stu-id="04a23-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="04a23-119">*lpfNeedsRestart*</span><span class="sxs-lookup"><span data-stu-id="04a23-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="04a23-120">Si este valor no es **null**, en la devolución solo será **true** si Windows debe reiniciarse para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="04a23-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a23-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04a23-121">Return value</span></span>

<span data-ttu-id="04a23-122">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04a23-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="04a23-123">Si no se produce ningún error, devuelve el código de **error \_ correcto** .</span><span class="sxs-lookup"><span data-stu-id="04a23-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a23-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04a23-124">Remarks</span></span>

<span data-ttu-id="04a23-125">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="04a23-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a23-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04a23-126">Requirements</span></span>



| <span data-ttu-id="04a23-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a23-127">Requirement</span></span> | <span data-ttu-id="04a23-128">Value</span><span class="sxs-lookup"><span data-stu-id="04a23-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a23-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04a23-129">DLL</span></span><br/> | <dl> <span data-ttu-id="04a23-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04a23-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
