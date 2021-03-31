---
description: COM+ incorpora apartamentos neutros para simplificar la programación en entornos multiproceso. El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Apartamentos neutros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423336"
---
# <a name="neutral-apartments"></a>Apartamentos neutros

COM+ incorpora apartamentos neutros para simplificar la programación en entornos multiproceso. El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.

En el pasado, para evitar cuellos de botella, los desarrolladores de COM+ que requieran la escalabilidad del servidor tenían que implementar componentes de subprocesamiento libre. sin embargo, los modelos de subprocesamiento libre son complicados de implementar porque deben tratar el acceso de interbloqueo. En apartamentos neutros, los objetos siguen las instrucciones para apartamentos multiproceso pero se pueden ejecutar en cualquier tipo de subproceso. Cuando un subproceso se ejecuta en un apartamento neutro, se recibe el contexto del objeto sin que se produzca un cambio de subproceso.

Cada proceso solo puede tener un apartamento neutro. Para seleccionar un apartamento neutro, utilice la siguiente configuración del registro:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

Los componentes que tienen interfaces de usuario deben seguir usando apartamentos de un solo subproceso como modelo preferido. Para seleccionar un contenedor uniproceso, utilice la siguiente configuración del registro:

**ThreadingModel** = Apartamento

 

 



