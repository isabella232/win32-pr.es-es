---
description: La propiedad DVDAdm proporciona acceso al objeto MSDVDAdm que contiene métodos y propiedades para guardar la información de la aplicación y del usuario.
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: Propiedad DVDAdm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adedea036393e68456cfd9f035882ae9c335063030518e808c57bced6d5b5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079165"
---
# <a name="dvdadm-property"></a>Propiedad DVDAdm

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm` propiedad proporciona acceso al objeto [MSDVDAdm](msdvdadm-object.md) que contiene métodos y propiedades para guardar información de usuario y aplicación.

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. No es necesario crear una referencia independiente al **objeto MSDVDAdm.** Para acceder a los métodos y propiedades del objeto , use la `DVDAdm` propiedad como se muestra en el ejemplo siguiente.

## <a name="examples"></a>Ejemplos


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



