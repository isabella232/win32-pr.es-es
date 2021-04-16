---
description: La función ShowJavaConsole es una ayuda para la depuración para los desarrolladores de Java. Las applets (u otro código Java) que se ejecutan en Internet Explorer pueden usarla para mostrar mensajes de error y otra información.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649827"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="12f9b-104">ShowJavaConsole función)</span><span class="sxs-lookup"><span data-stu-id="12f9b-104">ShowJavaConsole function</span></span>

<span data-ttu-id="12f9b-105">La función **ShowJavaConsole** es una ayuda para la depuración para los desarrolladores de Java.</span><span class="sxs-lookup"><span data-stu-id="12f9b-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="12f9b-106">Las applets (u otro código Java) que se ejecutan en Internet Explorer pueden usarla para mostrar mensajes de error y otra información.</span><span class="sxs-lookup"><span data-stu-id="12f9b-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f9b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12f9b-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="12f9b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12f9b-108">Parameters</span></span>

<span data-ttu-id="12f9b-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="12f9b-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="12f9b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12f9b-110">Return value</span></span>

<span data-ttu-id="12f9b-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="12f9b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12f9b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12f9b-112">Remarks</span></span>

<span data-ttu-id="12f9b-113">La llamada a **ShowJavaConsole** hace que la máquina virtual Java muestre la ventana de la consola Java.</span><span class="sxs-lookup"><span data-stu-id="12f9b-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="12f9b-114">La propia ventana de la consola Java puede mostrar la salida de depuración del código Java que se ejecuta en el proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="12f9b-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="12f9b-115">Normalmente, solo lo usaría una aplicación que hospeda la máquina virtual Java.</span><span class="sxs-lookup"><span data-stu-id="12f9b-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="12f9b-116">Solo hay una ventana de consola de Java por cada proceso. varias llamadas a la API provocan que se muestre la misma ventana.</span><span class="sxs-lookup"><span data-stu-id="12f9b-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="12f9b-117">En otras palabras, si ya se muestra la ventana de la consola, no sucede nada; Si la ventana no se ha mostrado o el usuario la ha cerrado, se abrirá la ventana.</span><span class="sxs-lookup"><span data-stu-id="12f9b-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="12f9b-118">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="12f9b-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f9b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f9b-119">Requirements</span></span>



| <span data-ttu-id="12f9b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f9b-120">Requirement</span></span> | <span data-ttu-id="12f9b-121">Value</span><span class="sxs-lookup"><span data-stu-id="12f9b-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12f9b-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12f9b-122">DLL</span></span><br/> | <dl> <span data-ttu-id="12f9b-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f9b-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
