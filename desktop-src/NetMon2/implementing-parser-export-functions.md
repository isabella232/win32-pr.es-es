---
description: Las funciones de exportación del analizador proporcionan toda la funcionalidad de los analizadores en el archivo DLL del analizador. Cada DLL del analizador debe implementar ParserAutoInstallInfo y DllMain. Las funciones de exportación restantes deben implementarse para cada analizador incluido en el archivo DLL del analizador.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementar funciones de exportación del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069332"
---
# <a name="implementing-parser-export-functions"></a>Implementar funciones de exportación del analizador

Las funciones de exportación del analizador proporcionan toda la funcionalidad de los analizadores en el archivo DLL del analizador. Cada DLL del analizador debe implementar [**ParserAutoInstallInfo**](parserautoinstallinfo.md) y [**DllMain**](dllmain-parser.md). Las funciones de exportación restantes deben implementarse para cada analizador incluido en el archivo DLL del analizador.

En los temas siguientes se muestra cómo implementar las funciones de exportación.



| Término                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementación de ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Proporciona una descripción y un ejemplo de código de la implementación de la función [**ParserAutoInstallInfo,**](parserautoinstallinfo.md) que identifica los analizadores ubicados en un archivo DLL del analizador.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementación del analizador de DllMain](implementing-dllmain-parser.md)<br/>                                    | Proporciona una descripción y un ejemplo de código de la implementación de la función Analizador de [**DllMain,**](dllmain-parser.md) que identifica la existencia de un analizador y, a continuación, libera los recursos que Monitor de red usa para el analizador.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementación del registro](implementing-register.md)<br/>                                                                  | Proporciona una descripción y un ejemplo de código de implementación de [**la función Register,**](register-parser.md) que registra todas las propiedades de un protocolo.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementación de RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Proporciona una descripción y un ejemplo de código de implementación de [**la función RecognizeFrame,**](recognizeframe.md) que identifica una instancia de un protocolo en un marco.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementación de AttachProperties](implementing-attachproperties.md)<br/>                          | Proporciona una descripción y un ejemplo de código de la implementación de la función [**AttachProperties,**](attachproperties.md) que separa los datos que reconoce el analizador y, a continuación, adjunta descripciones de propiedades a cada propiedad de protocolo que existe en los datos reconocidos.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementación de FormatProperties](implementing-formatproperties.md)<br/>                          | Proporciona una descripción y un ejemplo de código de implementación de la función [**FormatProperties,**](formatproperties.md) que da formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementación de Anulación del registro](implementing-deregister.md)<br/>                                                        | Proporciona una descripción y un ejemplo de código de implementación de la [**función Deregister,**](deregister.md) que libera los recursos usados para registrar las propiedades del protocolo.<br/>                                                                                                     |



 

 

 




