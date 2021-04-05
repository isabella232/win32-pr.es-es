---
description: Módulos de TopoEdit
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: Módulos de TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082433"
---
# <a name="topoedit-modules"></a>Módulos de TopoEdit

La herramienta TopoEdit se proporciona con el Windows SDK para Windows Server 2008 y versiones posteriores. La herramienta requiere Windows Vista o posterior.

Los módulos TopoEdit se encuentran en la carpeta bin del SDK de. Estos módulos son:

-   TopoEdit.exe: ejecutable de la aplicación
-   TEDUTIL.dll: DLL de extensión

La instalación del SDK registra el archivo DLL. Sin embargo, si se produce un error, en un símbolo del sistema, ejecute lo siguiente.


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



El código fuente de TopoEdit también se proporciona como un ejemplo en el Windows SDK. Se encuentra en el siguiente directorio:

<samples root>\\Multimedia \\ Media Foundation \\ TopoEdit

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a TopoEdit](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



