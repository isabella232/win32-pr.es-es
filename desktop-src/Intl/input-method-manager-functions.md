---
description: En esta sección se describen las funciones de IMM.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Funciones del administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516a83e207434f5d8c2e073e770c878198bc98e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667555"
---
# <a name="input-method-manager-functions"></a>Funciones del administrador de métodos de entrada

En esta sección se describen las funciones de IMM.



| Función                                                           | Descripción                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Devuelve un puntero a una interfaz [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon) .                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Devuelve un puntero a una interfaz [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary) .                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Devuelve un puntero a una interfaz [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage) .                                                      |
| [**EnumInputContext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Función de devolución de llamada definida por la aplicación que procesa los contextos de entrada proporcionados por la función **ImmEnumInputContext** .   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Función de devolución de llamada definida por la aplicación que se usa con la función **ImmEnumRegisterWord** .                                   |
| [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Asocia el contexto de entrada especificado a la ventana especificada.                                                          |
| [**ImmAssociateContextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Cambia la asociación entre el contexto del método de entrada y la ventana especificada o sus elementos secundarios.                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Muestra el cuadro de diálogo de configuración para el IME del identificador de configuración regional de entrada especificado.                                |
| [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Crea un nuevo contexto de entrada, asignando memoria para el contexto e inicializando.                                        |
| [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Libera el contexto de entrada y libera la memoria asociada.                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Deshabilita el IME para un subproceso o para todos los subprocesos de un proceso.                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Indica que este subproceso es un subproceso de interfaz de usuario de la aplicación de la tienda Windows.                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | En desuso. Deshabilita el servicio de texto para el subproceso especificado.                                                            |
| [**ImmEnumInputContext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Recupera el contexto de entrada para el subproceso especificado.                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Enumera las cadenas de registro que tienen la cadena de lectura, el estilo y la cadena de registro especificados.                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Obtiene acceso a las capacidades de IME particulares que no están disponibles a través de otras funciones de la API de IME.                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Recupera una lista de candidatos.                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Recupera el tamaño de las listas de candidatos.                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Recupera información sobre la ventana candidatos.                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Recupera información sobre la fuente lógica utilizada actualmente para mostrar caracteres en la ventana de composición.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Recupera información sobre la cadena de composición.                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Recupera información sobre la ventana de composición.                                                                        |
| [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Recupera el contexto de entrada asociado a la ventana especificada.                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Recupera la lista de resultados de la conversión de caracteres o palabras sin generar ningún mensaje relacionado con el IME.                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Recupera el estado de conversión actual.                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Recupera el identificador de ventana predeterminado de la clase IME.                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Copia la descripción del IME en el búfer especificado.                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Recupera información sobre los errores.                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Recupera el nombre de archivo del IME asociado a la configuración regional de entrada especificada.                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Recupera los elementos de menú que están registrados en el menú del IME de un contexto de entrada especificado.                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Determina si el IME está abierto o cerrado.                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Recupera la propiedad y las capacidades del IME asociado a la configuración regional de entrada especificada.                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Recupera una lista de los estilos admitidos por el IME asociado a la configuración regional de entrada especificada.                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Recupera la posición de la ventana de estado.                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Recupera el valor de clave virtual original asociado a un mensaje de entrada de clave que el IME ya ha procesado.           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Instala un IME.                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Determina si la configuración regional de entrada especificada tiene un IME.                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Comprueba los mensajes destinados a la ventana del IME y envía esos mensajes a la ventana especificada.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Notifica al IME sobre los cambios en el estado del contexto de entrada.                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Registra una cadena con el Diccionario del IME asociado a la configuración regional de entrada especificada.                              |
| [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Libera el contexto de entrada y desbloquea la memoria asociada en el contexto de entrada.                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Solicita un mensaje de la aplicación.                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Establece información sobre la ventana candidatos.                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Establece la fuente lógica que se va a usar para mostrar los caracteres en la ventana de composición.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Establece los caracteres, atributos y cláusulas de las cadenas de composición y lectura.                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Establece la posición de la ventana de composición.                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Establece el estado de la conversión actual.                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Abre o cierra el IME.                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Establece la posición de la ventana de estado.                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simula la tecla de acceso rápido del IME especificada, lo que produce la misma respuesta que si el usuario presiona la tecla de acceso rápido en la ventana especificada. |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Quita una cadena de registro del Diccionario del IME asociado a la configuración regional de entrada especificada.                       |



 

 

 



