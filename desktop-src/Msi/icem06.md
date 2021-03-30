---
description: ICEM06 comprueba las referencias directas no válidas a las características del módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910381"
---
# <a name="icem06"></a>ICEM06

ICEM06 comprueba las referencias directas no válidas a las características del módulo.

El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.

## <a name="result"></a>Resultado

ICEM06 expone un error cuando la base de datos del módulo contiene referencias directas a una característica. El usuario del módulo debe proporcionar la información de características.

## <a name="example"></a>Ejemplo

ICEM06 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo          | Destino                                 |
|-------------------|----------------------------------------|
| Shortcut1. *GUID1* | cmd.exe                                |
| Shortcut2. *GUID1* | \[Propiedades de\]                             |
| Shortcut3. *GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID   | Context       | Componente\_ | Característica\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | Mi característica                              |



 

ICEM06 informa del primer error porque el primer registro de la tabla de acceso directo tiene una entrada en el campo de destino que no es una propiedad o un GUID nulo. Un módulo no puede hacer referencia directamente a una característica. El usuario del módulo debe proporcionar la información de características. Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.

ICEM06 informa del segundo error porque el segundo registro de la tabla de la clase tiene una entrada en el campo de característica que no es un GUID nulo. Un módulo no puede hacer referencia directamente a una característica. El usuario del módulo debe proporcionar la información de características. Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



