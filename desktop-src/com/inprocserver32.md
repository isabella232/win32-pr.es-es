---
title: InprocServer32
description: Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Com de clave del Registro InprocServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060910"
---
# <a name="inprocserver32"></a>InprocServer32

Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a>Observaciones

**ThreadingModel** es un **valor \_ REG SZ** que especifica el modelo de subprocesos. Los valores posibles se muestran en la tabla siguiente.



| Value     | Descripción                                |
|-----------|--------------------------------------------|
| Apartamento | Apartamento de un solo subproceso                  |
| Ambos      | Un solo subproceso o un apartamento multiproceso |
| Gratuito      | Apartamento multiproceso                    |
| Neutra   | Apartamento neutro                          |



 

Debe usar el mismo valor para cada objeto proporcionado por el servidor en proceso.

Si **ThreadingModel** no está presente o no está establecido en un valor, el servidor se carga en el primer apartamento que se inicializó en el proceso. Este apartamento se conoce a veces como el apartamento principal de un solo subproceso (STA). Si com inicializa el primer STA de un proceso, en lugar de hacerlo mediante una llamada explícita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)se denomina STA del host. Por ejemplo, COM crea un STA de host si un servidor en proceso que se va a cargar requiere un STA, pero actualmente no hay ningún STA en el proceso.

Siempre que sea posible, el servidor en proceso se carga en el mismo apartamento que el cliente que lo carga. Si el modelo de subprocesos del apartamento cliente no es compatible con el modelo especificado, el servidor se carga como se indica en la tabla siguiente.



| Modelo de subprocesos del servidor | El servidor de Apartamento se ejecuta en |
|---------------------------|----------------------------|
| <not specified>     | Sta principal                   |
| Ambos                      | El mismo apartamento que el cliente   |
| Gratuito                      | Apartamento multiproceso    |
| Neutra                   | Apartamento neutro          |



 

Si el modelo de subprocesos del servidor es Apartment, el apartamento en el que se carga el servidor depende del apartamento en el que se ejecuta el cliente, como se indica en la tabla siguiente.



| El cliente de Apartment se ejecuta en | El servidor de Apartamento se ejecuta en |
|----------------------------|----------------------------|
| Multiproceso              | Host STA                   |
| Neutral (en subproceso STA)    | El mismo apartamento que el cliente   |
| Neutral (en subproceso MTA)    | Host STA                   |



 

COM también puede crear un apartamento multiproceso de host (MTA). Si un cliente de un solo subproceso solicita un servidor en proceso cuyo modelo de subprocesamiento es Gratis cuando no hay MTA en el proceso, COM crea un MTA host y carga el servidor en él.

Para un servidor en proceso de 32 bits, se deben registrar las claves [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32** e [**Insertable.**](insertable.md) La **entrada InprocServer** solo es necesaria para la compatibilidad con versiones anteriores. Si falta, la clase sigue funcionando, pero no se puede cargar en aplicaciones de 16 bits.

Si un contenedor busca en el Registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




