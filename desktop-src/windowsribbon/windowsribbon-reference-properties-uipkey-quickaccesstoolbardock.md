---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la propiedad QuickAccessToolbarDock de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420796"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="cd46f-103">UI \_ PKEY \_ QuickAccessToolbarDock</span><span class="sxs-lookup"><span data-stu-id="cd46f-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="cd46f-104">Identifica la propiedad QuickAccessToolbarDock de PKEY de la interfaz de usuario \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cd46f-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="cd46f-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd46f-105">Remarks</span></span>

<span data-ttu-id="cd46f-106">\_ \_ Una aplicación usa la interfaz de usuario PKEY QuickAccessToolbarDock para consultar el estado de acoplamiento de la barra de herramientas de acceso rápido (Qat).</span><span class="sxs-lookup"><span data-stu-id="cd46f-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="cd46f-107">El valor de la propiedad es de la enumeración [**\_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cd46f-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd46f-108">CONTROLDOCK de IU \_ \_ superior</span><span class="sxs-lookup"><span data-stu-id="cd46f-108">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="cd46f-109">El QAT se acopla en el área no cliente de la aplicación host de la cinta de opciones, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cd46f-109">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![captura de pantalla de la barra de herramientas de acceso rápido acoplada encima de la cinta de opciones en el área no cliente.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="cd46f-111">CONTROLDOCK de IU \_ \_ inferior</span><span class="sxs-lookup"><span data-stu-id="cd46f-111">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="cd46f-112">El QAT se acopla como una banda entera visualmente debajo de la cinta de opciones, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cd46f-112">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="cd46f-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cd46f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd46f-115">Propiedades de la cinta</span><span class="sxs-lookup"><span data-stu-id="cd46f-115">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

