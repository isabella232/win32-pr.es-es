---
title: Modificador /target
description: El modificador /target permite al compilador MIDL habilitar las optimizaciones disponibles solo en versiones recientes de Windows. El modificador /target activa automáticamente modificadores adicionales.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /target switch MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159701"
---
# <a name="target-switch"></a>Modificador /target

El **modificador /target** permite que el compilador MIDL habilite las optimizaciones disponibles solo en versiones recientes de Windows. El **modificador /target** activa automáticamente modificadores adicionales.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de destino, como NT50, NT51, NT60, NT61, NT62 o NT100.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /target** activa automáticamente modificadores adicionales, en función del sistema operativo, como se especifica en la tabla siguiente:



| Sistema operativo | /target level | Conmutadores activados                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf /error all /robust               |
| Windows XP       | NT51          | /Oicf /error all /robust /protocol all |
| Windows Vista    | NT60          | /Oicf /error all /robust /protocol all |
| Windows 7        | NT61          | /Oicf /error all /robust /protocol all |
| Windows 8        | NT62          | /Oicf /error all /robust /protocol all |
| Windows 10       | NT100         | /Oicf /error all /robust /protocol all |
 

Para asegurarse de que un código auxiliar se ejecuta en el sistema especificado por el modificador **/target,** MIDL emite un error cuando una característica disponible solo en una versión más reciente de Windows está presente. En la tabla siguiente se especifica el nivel **mínimo /target** necesario para habilitar la característica. Los niveles de destino más altos incluyen todas las características de los niveles de destino inferiores.



| Nivel mínimo requerido /target | Características                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /robust<br/> \[message\]<br/> \[async\]<br/> \[uuid \_ asincrónico\]<br/> \[notificar \] en modo /Oicf<br/> \[codificar \] o \[ descodificar en modo \] /Oicf<br/>                   |
| NT51                           | Compatibilidad con /protocol de 64 bits<br/> \[partial \_ ignore\]<br/> \[forzar \_ asignación\]<br/>                                                                                                 |
| NT60                           | Marshalling de estructuras complejas forzadas<br/> Identificadores de contexto en una matriz o estructura<br/> \[Compatibilidad \] con intervalos para cadenas sin formato<br/> \[identificador \_ de contexto estricto de \_ \_ tipo\]<br/> |
| NT61                           | Las llamadas directas de código auxiliar COM para interfaces con menos de 32 métodos requieren la vinculación de códigos auxiliares COM **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Compatibilidad con ARM<br/> Compatibilidad con WinRT<br/>                                                                                                                                                   |
| NT100                          | \[system_handle \] compatibilidad<br /> |


 

## <a name="examples"></a>Ejemplos

**midl /target NT50**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
