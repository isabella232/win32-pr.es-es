---
description: La propiedad DisableAutoMouseProcessing habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propiedad DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494398"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="31410-103">Propiedad DisableAutoMouseProcessing</span><span class="sxs-lookup"><span data-stu-id="31410-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="31410-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="31410-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="31410-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="31410-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="31410-106">La `DisableAutoMouseProcessing` propiedad habilita o deshabilita la funcionalidad de procesamiento del mouse del objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="31410-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="31410-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31410-107">Return Value</span></span>

<span data-ttu-id="31410-108">Devuelve un valor booleano que indica si se va a deshabilitar el procesamiento predeterminado del mouse.</span><span class="sxs-lookup"><span data-stu-id="31410-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="31410-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31410-109">Remarks</span></span>

<span data-ttu-id="31410-110">Esta propiedad es de lectura/escritura y su valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="31410-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="31410-111">El objeto **MSWebDVD** controla automáticamente las acciones del mouse para los menús en pantalla de DVD de forma predeterminada. los usuarios pueden resaltar y activar los botones de menú sin necesidad de programación especial por parte de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31410-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="31410-112">Una aplicación puede desactivar esta funcionalidad predeterminada de control del mouse estableciendo esta propiedad en **true**.</span><span class="sxs-lookup"><span data-stu-id="31410-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="31410-113">Cuando el procesamiento automático del mouse está desactivado, una aplicación debe usar los distintos métodos y propiedades relacionados con el botón para controlar los movimientos del mouse y los clics del mouse en los menús en pantalla.</span><span class="sxs-lookup"><span data-stu-id="31410-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="31410-114">Además, una aplicación puede usar los métodos relacionados con el botón para invalidar el control automático del mouse incluso cuando `DisableAutoMouseProcessing` se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="31410-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



