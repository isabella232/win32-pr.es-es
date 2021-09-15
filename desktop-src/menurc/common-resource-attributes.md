---
title: Atributos de recursos comunes
description: Las instrucciones de definición de recursos admitidas en las instrucciones de 16 bits Windows incluyen una opción load-mem que especifica las características de carga y memoria del recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359720"
---
# <a name="common-resource-attributes"></a>Atributos de recursos comunes

Las instrucciones de definición de recursos admitidas en las instrucciones de 16 Windows incluyen una opción *load-mem* que especifica las características de carga y memoria del recurso. Estos atributos se permiten en los scripts de recursos por compatibilidad con versiones anteriores, pero se omiten. Windows recursos se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.

## <a name="load-attributes"></a>Atributos de carga

Los atributos de carga especifican cuándo se va a cargar el recurso. El parámetro load debe ser uno de los atributos siguientes.



| Atributo      | Descripción                                                                  |
|----------------|------------------------------------------------------------------------------|
| **PRECARGA**    | ignorado. En los archivos Windows 16 bits, el recurso se carga con el archivo ejecutable. |
| **LOADONCALL** | ignorado. En la versión de 16 Windows, el recurso se carga cuando se llama a .              |



 

## <a name="memory-attributes"></a>Atributos de memoria

Los atributos de memoria especifican si el recurso es fijo o móvil, si se puede descartar y si es puro. El parámetro memory puede ser uno o varios de los atributos siguientes.



| Atributo       | Descripción                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | ignorado. En 16 bits Windows, el recurso permanece en una ubicación de memoria fija.                                                              |
| **MOVIBLE**    | ignorado. En el caso de Windows 16 bits, el recurso se puede mover si es necesario para compactar la memoria.                                                     |
| **DESCARTABLE** | ignorado. En las Windows de 16 bits, el recurso se puede descartar si ya no es necesario.                                                            |
| **PURO**        | ignorado. Se acepta por compatibilidad con scripts de recursos existentes.                                                                       |
| **IMPURO**      | ignorado. Se acepta por compatibilidad con scripts de recursos existentes.                                                                       |
| **COMPARTIDO**      | ignorado. En el caso de los módulos Windows 16 bits, SHARED se omite para los módulos normales. Para un recurso de un módulo de Windows ROM, se comparte la memoria.        |
| **NONSHARED**   | ignorado. En los módulos normales Windows 16 bits, NONSHARED se omite. Para un recurso de un módulo de Windows ROM, la memoria no se comparte. |



 

 

 




