---
description: Las funciones auxiliares expertos proporcionadas por Monitor de red y las funciones auxiliares comunes usan las estructuras descritas en la tabla siguiente.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Estructuras de expertos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16accf769b0983b782a6e6dbd723dd08df27415220bda1d59122b951439bac65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939022"
---
# <a name="expert-structures"></a>Estructuras de expertos

Las funciones auxiliares expertos proporcionadas por Monitor de red y las funciones auxiliares comunes usan las estructuras descritas en la tabla siguiente.



| Estructura                                              | Descripción                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Asocia un archivo DLL experto a su configuración.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Proporciona datos de configuración sin procesar.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Proporciona información sobre el archivo DLL experto. Monitor de red usa la información.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Proporciona información sobre un marco.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Proporciona información de inicio sobre el experto.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Proporciona el estado actual de un experto en ejecución.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Define las características del filtro de visualización para un experto.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Proporciona información sobre una línea mostrada en el visor experto.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Proporciona información que define una columna en el Visor de eventos.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Proporciona un contenedor para todos los datos posibles insertados en una columna en una línea del Visor de eventos.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Punto de entrada de la variante que indica qué elemento de la unión se va a usar y cómo dar formato a él. |



 

Monitor de red también proporciona funciones de exportación (funciones auxiliares a las que el experto puede llamar) y enumeraciones.



| Para información acerca de                                          | Vea                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportar funciones que proporcionan puntos de entrada al archivo DLL experto. | [Funciones de exportación de DLL expertos](expert-dll-export-functions.md)               |
| Funciones auxiliares a las que pueden llamar expertos y analizadores.    | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo llaman expertos.              | [Funciones expertos](expert-functions.md)                                     |
| Enumeraciones utilizadas por estructuras y funciones expertos.          | [Enumeraciones de expertos](expert-enumerations.md)                               |



 

 

 



