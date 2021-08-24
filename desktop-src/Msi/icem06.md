---
description: ICEM06 busca referencias directas no válidas a las características del módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5150e511e6f8018e51ab537b52ccc6c32645d09c80110129f040d6a329335ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828885"
---
# <a name="icem06"></a>ICEM06

ICEM06 busca referencias directas no válidas a las características del módulo.

Los ICE del módulo de mezcla se almacenan en un archivo .uu. del módulo de mezcla denominado Mergemod.pack y no en el archivo .uu. que contiene los ICE usados para la validación del paquete.

## <a name="result"></a>Resultado

ICEM06 publica un error cuando la base de datos del módulo contiene referencias directas a una característica. El usuario del módulo debe proporcionar información de características.

## <a name="example"></a>Ejemplo

ICEM06 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo          | Destino                                 |
|-------------------|----------------------------------------|
| Acceso directo1. *GUID1* | cmd.exe                                |
| Acceso directo2. *GUID1* | \[MyProp\]                             |
| Acceso directo3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID   | Contexto       | Componente\_ | Característica\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Componente1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Componente 2  | MyFeature                              |



 

ICEM06 notifica el primer error porque el primer registro de la tabla Acceso directo tiene una entrada en el campo Destino que no es una propiedad o un GUID nulo. Un módulo no puede hacer referencia a una característica directamente. El usuario del módulo debe proporcionar información de características. Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.

ICEM06 notifica el segundo error porque el segundo registro de la tabla Clase tiene una entrada en el campo Característica que no es un GUID nulo. Un módulo no puede hacer referencia a una característica directamente. El usuario del módulo debe proporcionar información de características. Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



