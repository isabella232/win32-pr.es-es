---
description: Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador. Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funciones de exportación de DLL de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423675"
---
# <a name="parser-dll-export-functions"></a>Funciones de exportación de DLL de analizador

Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador. Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.



| Función                                           | Descripción                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Analizador de DllMain](dllmain-parser.md)               | Indica al archivo DLL del analizador que está cargado o descargado. El sistema operativo llama a la función de **analizador DllMain** cuando un proceso carga o descarga el archivo dll. |
| [AttachProperties](attachproperties.md)           | Notifica al analizador que debe adjuntar cualquier propiedad que exista en un marco.                                                                                            |
| [Eliminar registro](deregister.md)                       | Notifica al analizador que se va a limpiar.                                                                                                                               |
| [FormatProperties](formatproperties.md)           | Notifica al analizador que debe tomar todas las instancias de propiedad de y compilar el miembro **szPropertyText** de cada estructura **PROPERTYINST** .                       |
| [RecognizeFrame](recognizeframe.md)               | Determina si el analizador puede interpretar los datos del marco sin procesar con el protocolo especificado.                                                            |
| [Registrar analizador](register-parser.md)             | Determina la información básica sobre el analizador en el archivo DLL. Monitor de red llama a la función **Register parser** .                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Instala un analizador automáticamente.                                                                                                                               |



 

Monitor de red proporciona las estructuras y las funciones auxiliares a las que puede llamar el analizador.



| Para más información sobre                          | Vea                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Funciones auxiliares a las que pueden llamar los expertos y analizadores. | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo pueden llamar los analizadores.        | [Funciones de analizador](parser-functions.md)                                     |
| Estructuras que usan las funciones de analizador.               | [Estructuras de analizador](parser-structures.md)                                   |



 

 

 



