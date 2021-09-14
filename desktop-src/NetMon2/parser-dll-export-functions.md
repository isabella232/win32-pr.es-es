---
description: Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador. Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funciones de exportación de DLL del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362140"
---
# <a name="parser-dll-export-functions"></a>Funciones de exportación de DLL del analizador

Las funciones, enumeradas en la tabla siguiente, son puntos de entrada para los archivos DLL del analizador. Las funciones son los puntos de entrada para las llamadas desde el sistema operativo y Monitor de red.



| Función                                           | Descripción                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Analizador de DllMain](dllmain-parser.md)               | Indica al archivo DLL del analizador que se carga o descarga. El sistema operativo llama a **la función DllMain Parser** cuando un proceso carga o descarga el archivo DLL. |
| [AttachProperties](attachproperties.md)           | Notifica al analizador que adjunte las propiedades que existen en un marco.                                                                                            |
| [Eliminar registro](deregister.md)                       | Notifica al analizador que limpie.                                                                                                                               |
| [FormatProperties](formatproperties.md)           | Notifica al analizador que tome todas las instancias de propiedad en y compile el **miembro szPropertyText** de cada **estructura PROPERTYINST.**                       |
| [RecognizeFrame](recognizeframe.md)               | Determina si el analizador puede interpretar los datos de fotogramas sin procesar con el protocolo especificado.                                                            |
| [Registrar analizador](register-parser.md)             | Determina la información básica sobre el analizador dentro del archivo DLL. Monitor de red llama a **la función Register Parser.**                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Instala automáticamente un analizador.                                                                                                                               |



 

Monitor de red proporciona estructuras y funciones auxiliares a las que el analizador puede llamar.



| Para más información sobre                          | Vea                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Funciones auxiliares a las que pueden llamar expertos y analizadores. | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |
| Funciones auxiliares a las que solo pueden llamar los analizadores.        | [Funciones del analizador](parser-functions.md)                                     |
| Estructuras que usan las funciones del analizador.               | [Estructuras del analizador](parser-structures.md)                                   |



 

 

 



