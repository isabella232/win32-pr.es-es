---
title: InprocServer32
description: Registra un servidor en proceso de 32 bits y especifica el modelo de subprocesos del apartamento en el que se puede ejecutar el servidor.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- Clave del registro InprocServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532344"
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

**ThreadingModel** es un valor de **reg \_ SZ** que especifica el modelo de subprocesos. Los valores posibles se muestran en la tabla siguiente.



| Value     | Descripción                                |
|-----------|--------------------------------------------|
| Procesamiento | Apartamento de un solo subproceso                  |
| Ambos      | Apartamento de un solo subproceso o multiproceso |
| Gratuito      | Apartamento multiproceso                    |
| Neutra   | Apartamento neutro                          |



 

Debe utilizar el mismo valor para todos los objetos proporcionados por el servidor en proceso.

Si **ThreadingModel** no está presente o no está establecido en un valor, el servidor se carga en el primer apartamento que se inicializó en el proceso. A veces, este apartamento se conoce como el contenedor uniproceso (STA) principal. Si COM inicializa el primer STA de un proceso, en lugar de una llamada explícita a [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), se denomina el STA del host. Por ejemplo, COM crea un STA de host si un servidor en proceso que se va a cargar requiere un STA, pero actualmente no hay ningún STA en el proceso.

Siempre que sea posible, el servidor en proceso se carga en el mismo contenedor que el cliente que lo carga. Si el modelo de subprocesos del apartamento de cliente no es compatible con el modelo especificado, el servidor se carga como se indica en la tabla siguiente.



| Modelo de subprocesos del servidor | El servidor de apartamento se ejecuta en |
|---------------------------|----------------------------|
| <not specified>     | STA principal                   |
| Ambos                      | Mismo apartamento que el cliente   |
| Gratuito                      | Apartamento multiproceso    |
| Neutra                   | Apartamento neutro          |



 

Si el modelo de subprocesos del servidor es apartamento, el apartamento en el que se carga el servidor depende del apartamento en el que se ejecuta el cliente, como se indica en la tabla siguiente.



| El cliente de contenedor se ejecuta en | El servidor de apartamento se ejecuta en |
|----------------------------|----------------------------|
| Multiproceso              | STA de host                   |
| Neutro (en el subproceso STA)    | Mismo apartamento que el cliente   |
| Neutro (en subproceso MTA)    | STA de host                   |



 

COM también puede crear un contenedor multiproceso (MTA) de host. Si un cliente de un contenedor uniproceso solicita un servidor en proceso cuyo modelo de subprocesos es gratuito cuando no hay ningún MTA en el proceso, COM crea un MTA de host y carga el servidor en él.

En el caso de un servidor de 32 bits en proceso, se deben registrar las claves [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InProcServer32** y que se pueden [**Insertar**](insertable.md) . La entrada **InprocServer** solo es necesaria para la compatibilidad con versiones anteriores. Si falta, la clase sigue funcionando, pero no se puede cargar en aplicaciones de 16 bits.

Si un contenedor está buscando en el registro un servidor en proceso, la versión de 16 bits tiene prioridad con un contenedor de 16 bits y la versión de 32 bits tiene prioridad con un contenedor de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**InprocServer**](inprocserver.md)
</dt> </dl>

 

 




