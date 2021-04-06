---
description: Las funciones auxiliares de expertos proporcionadas por Monitor de red y las funciones auxiliares comunes usan las estructuras descritas en la tabla siguiente.
ms.assetid: 3c49dd0a-836f-43f1-b383-357e8ba6545f
title: Estructuras expertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b9da00a71c3cdb9defe4396f4339f750cca359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000943"
---
# <a name="expert-structures"></a>Estructuras expertas

Las funciones auxiliares de expertos proporcionadas por Monitor de red y las funciones auxiliares comunes usan las estructuras descritas en la tabla siguiente.



| Estructura                                              | Descripción                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**CONFIGUREDEXPERT**](configuredexpert.md)           | Asocia un archivo DLL experto a su configuración.                                                       |
| [**EXPERTCONFIG**](expertconfig.md)                   | Proporciona datos de configuración sin procesar.                                                                       |
| [**EXPERTENUMINFO**](expertenuminfo.md)               | Proporciona información sobre el archivo DLL de expertos. Monitor de red usa la información.                       |
| [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) | Proporciona información sobre un marco.                                                                    |
| [**EXPERTSTARTUPINFO**](expertstartupinfo.md)         | Proporciona información de inicio sobre el experto.                                                         |
| [**EXPERTSTATUS**](expertstatus.md)                   | Proporciona el estado actual de un experto en ejecución.                                                       |
| [**FILTEROBJECT**](filterobject.md)                   | Define las características del filtro de presentación para un experto.                                              |
| [**NMEVENTDATA**](nmeventdata.md)                     | Proporciona información sobre una línea que se muestra en el visor de expertos.                                      |
| [**NMCOLUMNINFO**](nmcolumninfo.md)                   | Proporciona información que define una columna en el Visor de eventos.                                        |
| [**NMCOLUMNVARIANT**](nmcolumnvariant.md)             | Proporciona un contenedor para todos los datos posibles insertados en una columna en una línea en el Visor de eventos.     |
| [**NMCOLUMNTYPE**](nmcolumntype.md)                   | Punto de entrada de la variante que indica qué elemento de la Unión se va a usar y cómo aplicarle formato. |



 

Monitor de red también proporciona funciones de exportación (funciones auxiliares a las que puede llamar el experto) y enumeraciones.



| Para información acerca de                                          | Vea                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------|
| Exportar funciones que proporcionan puntos de entrada a su archivo DLL de expertos. | [Funciones de exportación de archivos DLL de experto](expert-dll-export-functions.md)               |
| Funciones auxiliares a las que pueden llamar expertos y analizadores.    | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo llaman expertos.              | [Funciones de experto](expert-functions.md)                                     |
| Enumeraciones usadas por las estructuras y funciones de expertos.          | [Enumeraciones de experto](expert-enumerations.md)                               |



 

 

 



