---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la propiedad \_ \_ QuickAccessToolbarDock de ui PKEY.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e28ec2e153755fd243bf78ee389cad40485a348
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443766"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="b8640-103">UI \_ PKEY \_ QuickAccessToolbarDock</span><span class="sxs-lookup"><span data-stu-id="b8640-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="b8640-104">Identifica la propiedad \_ \_ QuickAccessToolbarDock de ui PKEY.</span><span class="sxs-lookup"><span data-stu-id="b8640-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="b8640-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8640-105">Remarks</span></span>

<span data-ttu-id="b8640-106">La \_ interfaz de usuario \_ PKEY QuickAccessToolbarDock la usa una aplicación para consultar el estado de acoplamiento de la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="b8640-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="b8640-107">El valor de propiedad es de la [**\_ enumeración CONTROLDOCK de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b8640-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|    <span data-ttu-id="b8640-108">Enumeración</span><span class="sxs-lookup"><span data-stu-id="b8640-108">Enumeration</span></span>                     |    <span data-ttu-id="b8640-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8640-109">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8640-110">UI \_ CONTROLDOCK \_ TOP</span><span class="sxs-lookup"><span data-stu-id="b8640-110">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="b8640-111">El QAT se acopla en el área no cliente de la aplicación host de la cinta de opciones, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b8640-111">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![captura de pantalla de la barra de herramientas de acceso rápido acoplada encima de la cinta de opciones en el área no cliente.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="b8640-113">PARTE \_ INFERIOR DEL PANEL DE CONTROL DE INTERFAZ DE \_ USUARIO</span><span class="sxs-lookup"><span data-stu-id="b8640-113">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="b8640-114">El QAT se acopla como una banda visualmente integral debajo de la cinta de opciones, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="b8640-114">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="b8640-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8640-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8640-117">Propiedades de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="b8640-117">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

