---
description: COM+ presenta departamentos neutros para simplificar la programación en entornos multiproceso. El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: NeutralEstes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beea8fbc3d007b26274d4a2b9d4cfd1ac0b604991ad9039b5053ccf534a5c6d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070435"
---
# <a name="neutral-apartments"></a>NeutralEstes

COM+ presenta departamentos neutros para simplificar la programación en entornos multiproceso. El apartamento neutro es el modelo preferido para COM+ para los componentes sin interfaz de usuario.

En el pasado, para evitar cuellos de botella, los desarrolladores de COM+ que requerían escalabilidad del servidor tenían que implementar componentes sin subprocesos. sin embargo, los modelos de subprocesamiento libre son complicados de implementar porque deben tratar con el acceso de interbloqueo. En los departamentos neutros, los objetos siguen las directrices para los departamentos multiproceso, pero se pueden ejecutar en cualquier tipo de subproceso. Cuando un subproceso se ejecuta en un apartamento neutro, el contexto del objeto se recibe sin provocar un modificador de subproceso.

Cada proceso solo puede tener un apartamento neutro. Para seleccionar un contenedor neutro, use la siguiente configuración del Registro:

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

Los componentes que tienen interfaces de usuario deben seguir usando los departamentos de un solo subproceso como modelo preferido. Para seleccionar un contenedor de un solo subproceso, use la siguiente configuración del Registro:

**ThreadingModel** = Apartment

 

 



