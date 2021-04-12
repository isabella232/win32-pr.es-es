---
description: Las siguientes funciones se usan con la interfaz de usuario multilingüe (MUI).
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: Funciones de la interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f082115b0b12bdf6d26923ed8fc941b89887723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155152"
---
# <a name="multilingual-user-interface-functions"></a>Funciones de la interfaz de usuario multilingüe

Las siguientes funciones se usan con la interfaz de usuario multilingüe (MUI).



| Función                                                                 | Descripción                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | Enumera los idiomas de la interfaz de usuario que están disponibles en el sistema operativo.                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | Una función definida por la aplicación que se usa con la función [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .                      |
| [**FreeMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | Disminuye el recuento de referencias de un módulo de recursos cargado por [ **LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**GetFileMUIInfo**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | Recupera información relacionada con recursos sobre un archivo.                                                                    |
| [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | Recupera la ruta de acceso a un archivo de recursos específico del idioma asociado al archivo LN proporcionado.                           |
| [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | Recupera los idiomas de interfaz de usuario preferidos del proceso.                                                                           |
| [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | Recupera el identificador de idioma del idioma de interfaz de usuario predeterminado del sistema, conocido como "idioma de instalación" en Windows Vista. |
| [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | Recupera los idiomas de interfaz de usuario preferidos del sistema.                                                                            |
| [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | Recupera los idiomas de interfaz de usuario preferidos del subproceso para el subproceso actual.                                                     |
| [**GetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | Devuelve el identificador de idioma del primer idioma de la interfaz de usuario para el subproceso actual.                            |
| [**GetUILanguageFallbackList**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | Obtiene una lista de reserva de los idiomas de interfaz de usuario representados como nombres de idioma.                                         |
| [**GetUILanguageInfo**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | Recupera una gran variedad de información sobre el idioma de la interfaz de usuario.                                                     |
| [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | Devuelve el identificador de idioma del idioma de la interfaz de usuario del usuario actual.                                          |
| [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | Recupera los idiomas preferidos de la interfaz de usuario.                                                                              |
| [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | Devuelve un identificador para los recursos específicos del idioma asociados a un archivo neutro específico del lenguaje (LN).            |
| [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | Establece los idiomas de interfaz de usuario preferidos para el proceso de la aplicación.                                                    |
| [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | Establece los idiomas de interfaz de usuario preferidos del subproceso.                                                                                 |
| [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | Establece el idioma de la interfaz de usuario preferida para el subproceso actual.                                                      |



 

 

 
