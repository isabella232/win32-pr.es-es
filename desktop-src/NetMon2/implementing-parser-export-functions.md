---
description: Las funciones de exportación del analizador proporcionan toda la funcionalidad de los analizadores en el archivo DLL del analizador. Cada DLL del analizador debe implementar ParserAutoInstallInfo y DllMain. Las funciones de exportación restantes se deben implementar para cada analizador incluido en el archivo DLL del analizador.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementar funciones de exportación de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540171"
---
# <a name="implementing-parser-export-functions"></a>Implementar funciones de exportación de analizador

Las funciones de exportación del analizador proporcionan toda la funcionalidad de los analizadores en el archivo DLL del analizador. Cada DLL del analizador debe implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md) y [**DllMain**](dllmain-parser.md). Las funciones de exportación restantes se deben implementar para cada analizador incluido en el archivo DLL del analizador.

En los temas siguientes se muestra cómo implementar las funciones de exportación.



| Término                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Proporciona una descripción y un ejemplo de código de la implementación de la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) , que identifica los analizadores ubicados en una DLL de analizador.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementar el analizador de DllMain](implementing-dllmain-parser.md)<br/>                                    | Proporciona una descripción y un ejemplo de código de la implementación de la función de [**analizador DllMain**](dllmain-parser.md) , que identifica la existencia de un analizador y, a continuación, libera los recursos que utiliza monitor de red para el analizador.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementación del registro](implementing-register.md)<br/>                                                                  | Proporciona una descripción y un ejemplo de código de la implementación de la función de [**registro**](register-parser.md) , que registra todas las propiedades de un protocolo.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementación de RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Proporciona una descripción y un ejemplo de código de la implementación de la función [**RecognizeFrame**](recognizeframe.md) , que identifica una instancia de un protocolo en un marco.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementación de AttachProperties](implementing-attachproperties.md)<br/>                          | Proporciona una descripción y un ejemplo de código de la implementación de la función [**AttachProperties**](attachproperties.md) , que separa los datos que reconoce el analizador y, a continuación, adjunta las descripciones de propiedades a cada propiedad de protocolo que existe en los datos reconocidos.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementación de FormatProperties](implementing-formatproperties.md)<br/>                          | Proporciona una descripción y un ejemplo de código de la implementación de la función [**FormatProperties**](formatproperties.md) , que da formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de monitor de red.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementación de unregister](implementing-deregister.md)<br/>                                                        | Proporciona una descripción y un ejemplo de código de la implementación de la función de [**eliminación de registro**](deregister.md) , que libera los recursos utilizados para registrar propiedades de protocolo.<br/>                                                                                                     |



 

 

 




