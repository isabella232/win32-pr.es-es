---
title: Licencias
description: Licencias
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794025"
---
# <a name="licensing"></a><span data-ttu-id="829ef-103">Licencias</span><span class="sxs-lookup"><span data-stu-id="829ef-103">Licensing</span></span>

<span data-ttu-id="829ef-104">Para incrustar los controles con licencia correctamente, los contenedores de controles ActiveX deben usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) en lugar de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="829ef-104">In order to embed licensed controls successfully, ActiveX control containers must use [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) instead of [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="829ef-105">Varias funciones auxiliares de creación y carga de OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) y [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) llaman explícitamente a **IClassFactory** y no a **IClassFactory2** y, por tanto, no se pueden usar para crear o cargar controles ActiveX con licencia.</span><span class="sxs-lookup"><span data-stu-id="829ef-105">Several OLE creation and loading helper functions ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) explicitly call **IClassFactory** and not **IClassFactory2**, and therefore cannot be used to create or load licensed ActiveX controls.</span></span> <span data-ttu-id="829ef-106">Los contenedores de controles ActiveX deben crear y cargar explícitamente controles ActiveX mediante **IClassFactory2**.</span><span class="sxs-lookup"><span data-stu-id="829ef-106">ActiveX control containers should explicitly create and load ActiveX Controls using **IClassFactory2**.</span></span>

 

 