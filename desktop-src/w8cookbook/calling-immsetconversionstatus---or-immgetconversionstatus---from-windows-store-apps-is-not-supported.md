---
title: No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows
description: No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791920"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="96ef2-103">No se admite la llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="96ef2-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="96ef2-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="96ef2-104">Platforms</span></span>

<dl> <span data-ttu-id="96ef2-105">Clientes: Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="96ef2-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="96ef2-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="96ef2-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="96ef2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="96ef2-107">Description</span></span>

<span data-ttu-id="96ef2-108">La llamada a ImmSetConversionStatus () o ImmGetConversionStatus () desde una aplicación de la tienda Windows no se admite y puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="96ef2-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="96ef2-109">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="96ef2-109">Manifestations</span></span>

<span data-ttu-id="96ef2-110">Al iniciarse la aplicación, el modo IME se establece en los valores predeterminados siguientes:</span><span class="sxs-lookup"><span data-stu-id="96ef2-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="96ef2-111">Panel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="96ef2-111">Software input panel</span></span> | <span data-ttu-id="96ef2-112">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="96ef2-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="96ef2-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="96ef2-113">KOR, JPN</span></span> | <span data-ttu-id="96ef2-114">Activado</span><span class="sxs-lookup"><span data-stu-id="96ef2-114">On</span></span>                   | <span data-ttu-id="96ef2-115">Off</span><span class="sxs-lookup"><span data-stu-id="96ef2-115">Off</span></span>               |
| <span data-ttu-id="96ef2-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="96ef2-116">CHS, CHT</span></span> | <span data-ttu-id="96ef2-117">Activado</span><span class="sxs-lookup"><span data-stu-id="96ef2-117">On</span></span>                   | <span data-ttu-id="96ef2-118">Activado</span><span class="sxs-lookup"><span data-stu-id="96ef2-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="96ef2-119">Solución</span><span class="sxs-lookup"><span data-stu-id="96ef2-119">Solution</span></span>

<span data-ttu-id="96ef2-120">Los desarrolladores pueden controlar el modo IME predeterminado especificando un valor de ámbito de entrada para el campo.</span><span class="sxs-lookup"><span data-stu-id="96ef2-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="96ef2-121">Cada IME determina el modo IME para un ámbito de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="96ef2-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="96ef2-122">Los desarrolladores no pueden especificar el modo IME.</span><span class="sxs-lookup"><span data-stu-id="96ef2-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="96ef2-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="96ef2-123">Resources</span></span>

-   [<span data-ttu-id="96ef2-124">InputScope (enumeración)</span><span class="sxs-lookup"><span data-stu-id="96ef2-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="96ef2-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="96ef2-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="96ef2-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="96ef2-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 