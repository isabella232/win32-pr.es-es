---
description: Las siguientes funciones son los puntos de entrada de los archivos dll expertos y las llamadas del sistema operativo y Monitor de red.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funciones de exportación de archivos DLL de experto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000944"
---
# <a name="expert-dll-export-functions"></a>Funciones de exportación de archivos DLL de experto

Las siguientes funciones son los puntos de entrada de los archivos dll expertos y las llamadas del sistema operativo y Monitor de red.



| Función                                   | Descripción                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Experto de DllMain**](dllmain-expert.md)   | Indica que se ha cargado o descargado el archivo DLL de expertos. Cuando un proceso carga o descarga el archivo DLL, el sistema operativo llama a la función [**DllMain**](/windows/desktop/Dlls/dllmain) . |
| [**Registrar experto**](register-expert.md) | Determina la información básica sobre el experto en el archivo DLL. Monitor de red llama a la función **Register** .                                                           |
| [**Configuración**](configure.md)             | Configura el experto en el archivo DLL. Monitor de red llama a la función de [**configuración**](configure.md) .                                                                 |
| [**Ejecutar**](run.md)                         | Inicia el experto en el archivo DLL. Monitor de red llama a la función de [**ejecución**](run.md) .                                                                                 |



 

Monitor de red también proporciona estructuras, enumeraciones y funciones auxiliares a las que puede llamar el experto.



| Para información acerca de                                      | Vea                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones auxiliares a las que pueden llamar expertos y analizadores | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo llaman expertos           | [Funciones de experto](expert-functions.md)                                     |
| Estructuras usadas por las funciones de expertos               | [Estructuras expertas](expert-structures.md)                                   |
| Enumeraciones usadas por las estructuras y funciones de expertos       | [Enumeraciones de experto](expert-enumerations.md)                               |



 

 

 
