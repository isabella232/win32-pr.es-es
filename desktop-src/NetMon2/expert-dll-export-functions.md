---
description: Las siguientes funciones son los puntos de entrada para los archivos DLL expertos y para las llamadas desde el sistema operativo y Monitor de red.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funciones de exportación de DLL expertos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327b36990ac377595b31b55ebc0ed57157fd8d411f690aff3378293f35e39e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911135"
---
# <a name="expert-dll-export-functions"></a>Funciones de exportación de DLL expertos

Las siguientes funciones son los puntos de entrada para los archivos DLL expertos y para las llamadas desde el sistema operativo y Monitor de red.



| Función                                   | Descripción                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DllMain Expert**](dllmain-expert.md)   | Indica que el archivo DLL experto se ha cargado o descargado. Cuando un proceso carga o descarga el archivo DLL, el sistema operativo llama a la [**función DllMain.**](/windows/desktop/Dlls/dllmain) |
| [**Register Expert**](register-expert.md) | Determina la información básica sobre el experto dentro del archivo DLL. Monitor de red llama a la **función Register.**                                                           |
| [**Configuración**](configure.md)             | Configura el experto dentro del archivo DLL. Monitor de red llama a la [**función Configure.**](configure.md)                                                                 |
| [**Ejecutar**](run.md)                         | Inicia el experto dentro del archivo DLL. Monitor de red llama a [**la función Run.**](run.md)                                                                                 |



 

Monitor de red también proporciona estructuras, enumeraciones y funciones auxiliares a las que el experto puede llamar.



| Para información acerca de                                      | Vea                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones auxiliares a las que pueden llamar expertos y analizadores | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo llaman expertos           | [Funciones expertos](expert-functions.md)                                     |
| Estructuras utilizadas por funciones expertos               | [Estructuras expertos](expert-structures.md)                                   |
| Enumeraciones usadas por funciones y estructuras expertos       | [Enumeraciones de expertos](expert-enumerations.md)                               |



 

 

 
