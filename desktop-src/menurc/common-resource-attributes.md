---
title: Atributos de recursos comunes
description: Las instrucciones de definición de recursos que se admiten en Windows de 16 bits incluyen una opción Load-MEM que especifica las características de carga y memoria del recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704693"
---
# <a name="common-resource-attributes"></a>Atributos de recursos comunes

Las instrucciones de definición de recursos que se admiten en Windows de 16 bits incluyen una opción *Load-MEM* que especifica las características de carga y memoria del recurso. Estos atributos se permiten en scripts de recursos para la compatibilidad con versiones anteriores, pero se omiten. Los recursos de Windows se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.

## <a name="load-attributes"></a>Cargar atributos

Los atributos de carga especifican Cuándo se va a cargar el recurso. El parámetro Load debe ser uno de los siguientes atributos.



| Atributo      | Descripción                                                                  |
|----------------|------------------------------------------------------------------------------|
| **CARGAR previamente**    | ignorado. En Windows de 16 bits, el recurso se carga con el archivo ejecutable. |
| **LOADONCALL** | ignorado. En Windows de 16 bits, el recurso se carga cuando se llama.              |



 

## <a name="memory-attributes"></a>Atributos de memoria

Los atributos de memoria especifican si el recurso es fijo o móvil, si es descartable y si es puro. El parámetro Memory puede ser uno o varios de los siguientes atributos.



| Atributo       | Descripción                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | ignorado. En Windows de 16 bits, el recurso permanece en una ubicación de memoria fija.                                                              |
| **MOVIBLE**    | ignorado. En Windows de 16 bits, el recurso se puede migrar si es necesario para compactar la memoria.                                                     |
| **DESCARTABLE** | ignorado. En Windows de 16 bits, el recurso se puede descartar si ya no se necesita.                                                            |
| **INCLUYA**        | ignorado. Aceptado por compatibilidad con scripts de recursos existentes.                                                                       |
| **IMPURAS**      | ignorado. Aceptado por compatibilidad con scripts de recursos existentes.                                                                       |
| **RECURSO**      | ignorado. En Windows de 16 bits, se omite SHARED en los módulos normales. Para un recurso de un módulo de Windows de ROM, se comparte la memoria.        |
| **NO compartidos**   | ignorado. En Windows de 16 bits, la Nonshared se omite para los módulos normales. En un recurso de un módulo de Windows de ROM, no se comparte la memoria. |



 

 

 




