---
description: Módulos TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361115"
---
# <a name="topoedit-modules"></a>Módulos TopoEdit

La herramienta TopoEdit se proporciona con el SDK Windows para Windows Server 2008 y versiones posteriores. La herramienta requiere Windows Vista o posterior.

Los módulos TopoEdit se encuentran en la carpeta Bin del SDK. Estos módulos son:

-   TopoEdit.exe: ejecutable de aplicación
-   TEDUTIL.dll: DLL de extensión

La instalación del SDK registra el archivo DLL. Sin embargo, si se produce un error, en un símbolo del sistema, ejecute lo siguiente.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



El código fuente de TopoEdit también se proporciona como ejemplo en Windows SDK. Se encuentra en el directorio siguiente:

<samples root>\\Multimedia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



