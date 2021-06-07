---
title: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows
description: No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443155"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="1a23e-103">No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde aplicaciones de la Tienda Windows</span><span class="sxs-lookup"><span data-stu-id="1a23e-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="1a23e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="1a23e-104">Platforms</span></span>

<dl> <span data-ttu-id="1a23e-105">Clientes: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1a23e-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="1a23e-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1a23e-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="1a23e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a23e-107">Description</span></span>

<span data-ttu-id="1a23e-108">No se admite la llamada a ImmSetConversionStatus() o ImmGetConversionStatus() desde una aplicación de la Tienda Windows y puede provocar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="1a23e-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="1a23e-109">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="1a23e-109">Manifestations</span></span>

<span data-ttu-id="1a23e-110">Al iniciar la aplicación, el modo IME se establece en los valores predeterminados siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a23e-110">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="1a23e-111">Panel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="1a23e-111">Software input panel</span></span> | <span data-ttu-id="1a23e-112">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="1a23e-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="1a23e-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="1a23e-113">KOR, JPN</span></span> | <span data-ttu-id="1a23e-114">Activado</span><span class="sxs-lookup"><span data-stu-id="1a23e-114">On</span></span>                   | <span data-ttu-id="1a23e-115">Desactivado</span><span class="sxs-lookup"><span data-stu-id="1a23e-115">Off</span></span>               |
| <span data-ttu-id="1a23e-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="1a23e-116">CHS, CHT</span></span> | <span data-ttu-id="1a23e-117">Activado</span><span class="sxs-lookup"><span data-stu-id="1a23e-117">On</span></span>                   | <span data-ttu-id="1a23e-118">Activado</span><span class="sxs-lookup"><span data-stu-id="1a23e-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="1a23e-119">Solución</span><span class="sxs-lookup"><span data-stu-id="1a23e-119">Solution</span></span>

<span data-ttu-id="1a23e-120">Los desarrolladores pueden controlar el modo IME predeterminado especificando un valor de ámbito de entrada para el campo.</span><span class="sxs-lookup"><span data-stu-id="1a23e-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="1a23e-121">Cada IME determina el modo IME para un ámbito de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="1a23e-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="1a23e-122">Los desarrolladores no pueden especificar el modo IME.</span><span class="sxs-lookup"><span data-stu-id="1a23e-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="1a23e-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="1a23e-123">Resources</span></span>

-   [<span data-ttu-id="1a23e-124">Enumeración InputScope</span><span class="sxs-lookup"><span data-stu-id="1a23e-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="1a23e-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="1a23e-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="1a23e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1a23e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 