---
title: Atributos de recursos comunes
description: Las instrucciones de definición de recursos admitidas en las instrucciones de 16 Windows incluyen una opción load-mem que especifica las características de carga y memoria del recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7bf01f95c700f12d130490673ef4f0df61cb84ae8077ca759655a2c4a1577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235582"
---
# <a name="common-resource-attributes"></a>Atributos de recursos comunes

Las instrucciones de definición de recursos admitidas en las instrucciones de 16 Windows incluyen una opción *load-mem* que especifica las características de carga y memoria del recurso. Estos atributos se permiten en los scripts de recursos por compatibilidad con versiones anteriores, pero se omiten. Windows recursos se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.

## <a name="load-attributes"></a>Cargar atributos

Los atributos de carga especifican cuándo se va a cargar el recurso. El parámetro load debe ser uno de los siguientes atributos.



| Atributo      | Descripción                                                                  |
|----------------|------------------------------------------------------------------------------|
| **Precarga**    | ignorado. En los archivos de 16 Windows, el recurso se carga con el archivo ejecutable. |
| **LOADONCALL** | ignorado. En los archivos de 16 Windows, el recurso se carga cuando se llama a .              |



 

## <a name="memory-attributes"></a>Atributos de memoria

Los atributos de memoria especifican si el recurso es fijo o móvil, si se puede descartar y si es puro. El parámetro memory puede ser uno o varios de los atributos siguientes.



| Atributo       | Descripción                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | ignorado. En los archivos de 16 Windows, el recurso permanece en una ubicación de memoria fija.                                                              |
| **Movible**    | ignorado. En los archivos de 16 Windows, el recurso se puede mover si es necesario para compactar la memoria.                                                     |
| **DESCARTABLE** | ignorado. En las Windows de 16 bits, el recurso se puede descartar si ya no es necesario.                                                            |
| **Puro**        | ignorado. Se acepta por compatibilidad con scripts de recursos existentes.                                                                       |
| **Impuro**      | ignorado. Se acepta por compatibilidad con scripts de recursos existentes.                                                                       |
| **Compartido**      | ignorado. En los módulos de 16 Windows, SHARED se omite para los módulos normales. Para un recurso de un módulo de Windows ROM, la memoria se comparte.        |
| **NONSHARED**   | ignorado. En los módulos de 16 Windows, NONSHARED se omite para los módulos normales. Para un recurso de un módulo de Windows ROM, la memoria no se comparte. |



 

 

 




