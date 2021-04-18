---
title: Registro propio para controles
description: Registro propio para controles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695768"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="2cfa8-103">Registro propio para controles</span><span class="sxs-lookup"><span data-stu-id="2cfa8-103">Self Registration for Controls</span></span>

<span data-ttu-id="2cfa8-104">Los controles ActiveX deben admitir el registro automático mediante la implementación de las funciones [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) .</span><span class="sxs-lookup"><span data-stu-id="2cfa8-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="2cfa8-105">Los controles ActiveX deben registrar todas las entradas del registro estándar para los objetos incrustables y los servidores de automatización.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="2cfa8-106">Los controles ActiveX deben usar la API de categorías de componentes para registrarse como control y registrar las categorías de componentes que requieren que un host admita y las categorías que el control implementa, vea [categorías de componentes](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="2cfa8-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="2cfa8-107">Los controles ActiveX también deben registrar la clave del registro [ToolBoxBitmap32](toolboxbitmap32.md) , aunque esto no es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="2cfa8-108">La categoría de componente insertable solo debe registrarse si el control es adecuado para su uso como un objeto de documento compuesto.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="2cfa8-109">Es importante tener en cuenta que un objeto de documento compuesto debe admitir ciertas interfaces más allá del valor [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) mínimo necesario para un control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="2cfa8-110">Aunque un control ActiveX puede calificarse como un objeto de documento compuesto, la documentación del control debe indicar claramente qué comportamiento esperar en estas circunstancias.</span><span class="sxs-lookup"><span data-stu-id="2cfa8-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cfa8-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cfa8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cfa8-112">Controles</span><span class="sxs-lookup"><span data-stu-id="2cfa8-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 