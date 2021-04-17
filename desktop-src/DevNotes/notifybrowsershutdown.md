---
description: Libera los cargadores de clase de Java que se pueden haber consumido al examinar las applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670812"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="7a631-103">NotifyBrowserShutdown función)</span><span class="sxs-lookup"><span data-stu-id="7a631-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="7a631-104">Libera los cargadores de clase de Java que se pueden haber consumido al examinar las applets.</span><span class="sxs-lookup"><span data-stu-id="7a631-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a631-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a631-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="7a631-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a631-107">*lpvReserved*</span><span class="sxs-lookup"><span data-stu-id="7a631-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="7a631-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="7a631-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a631-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a631-109">Return value</span></span>

<span data-ttu-id="7a631-110">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7a631-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="7a631-111">De lo contrario, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="7a631-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a631-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a631-112">Remarks</span></span>

<span data-ttu-id="7a631-113">Cuando el recuento de ventanas del explorador llega a cero en el modo Web integrado, esta función libera los cargadores de la clase Java.</span><span class="sxs-lookup"><span data-stu-id="7a631-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="7a631-114">Cuando el usuario empiece a examinar de nuevo las applets, la máquina virtual de Java descargará los archivos de clase más recientes.</span><span class="sxs-lookup"><span data-stu-id="7a631-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="7a631-115">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7a631-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a631-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a631-116">Requirements</span></span>



| <span data-ttu-id="7a631-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a631-117">Requirement</span></span> | <span data-ttu-id="7a631-118">Value</span><span class="sxs-lookup"><span data-stu-id="7a631-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a631-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a631-119">DLL</span></span><br/> | <dl> <span data-ttu-id="7a631-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a631-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
