---
description: El instalador puede aumentar la resistencia de la aplicación reinstalando automáticamente los componentes dañados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Buscar una característica o componente interrumpido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277367"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="7bc1b-103">Buscar una característica o componente interrumpido</span><span class="sxs-lookup"><span data-stu-id="7bc1b-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="7bc1b-104">El instalador puede aumentar la [resistencia](resiliency.md) de la aplicación reinstalando automáticamente los componentes dañados.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="7bc1b-105">En concreto, el instalador vuelve a instalar un componente o una característica si encuentra que falta el archivo o la clave del registro especificados en la columna de ruta de acceso de la [tabla de componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc1b-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="7bc1b-106">Si la ruta de acceso del componente de una característica está dañada en el origen, o si se produce un error en la forma en que se crea la ruta de acceso de la base de datos, es posible que el instalador intente abrir un paquete de instalación y reinstale la característica cada vez que se active el método abreviado de la característica.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="7bc1b-107">Para determinar la causa de los intentos repetidos de reinstalar una característica o aplicación, busque en el registro de eventos dos entradas como la siguiente.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="7bc1b-108">El primer mensaje indica qué componente del paquete del producto se estaba instalando.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="7bc1b-109">Este es el componente al que se hace referencia en la \_ columna componente de la [tabla de acceso directo](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="7bc1b-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="7bc1b-110">El segundo mensaje indica qué componente está detectando errores.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="7bc1b-111">Este es el componente con la ruta de la ruta de rutas que falta o está dañada y que desencadena la reinstalación.</span><span class="sxs-lookup"><span data-stu-id="7bc1b-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



