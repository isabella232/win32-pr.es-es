---
description: La propiedad DVDAdm proporciona acceso al objeto MSDVDAdm que contiene métodos y propiedades para guardar la información de la aplicación y del usuario.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propiedad DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152357"
---
# <a name="dvdadm-property"></a><span data-ttu-id="d502e-103">Propiedad DVDAdm</span><span class="sxs-lookup"><span data-stu-id="d502e-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="d502e-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d502e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d502e-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d502e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d502e-106">La `DVDAdm` propiedad proporciona acceso al objeto [MSDVDAdm](msdvdadm-object.md) que contiene métodos y propiedades para guardar la información de la aplicación y del usuario.</span><span class="sxs-lookup"><span data-stu-id="d502e-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="d502e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d502e-107">Remarks</span></span>

<span data-ttu-id="d502e-108">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d502e-108">This property is read-only with no default value.</span></span> <span data-ttu-id="d502e-109">No es necesario crear una referencia independiente al objeto **MSDVDAdm** .</span><span class="sxs-lookup"><span data-stu-id="d502e-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="d502e-110">Para tener acceso a los métodos y las propiedades del objeto, utilice la `DVDAdm` propiedad tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d502e-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="d502e-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d502e-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



