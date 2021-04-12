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
# <a name="dvdadm-property"></a>Propiedad DVDAdm

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm` propiedad proporciona acceso al objeto [MSDVDAdm](msdvdadm-object.md) que contiene métodos y propiedades para guardar la información de la aplicación y del usuario.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. No es necesario crear una referencia independiente al objeto **MSDVDAdm** . Para tener acceso a los métodos y las propiedades del objeto, utilice la `DVDAdm` propiedad tal y como se muestra en el ejemplo siguiente.

## <a name="examples"></a>Ejemplos


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



