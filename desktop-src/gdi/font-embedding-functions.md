---
description: Las siguientes funciones se usan con fuentes OpenType de Microsoft incrustadas.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Funciones de incrustación de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ece5b413be5489bf51df38fd92b6f3167823506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997384"
---
# <a name="font-embedding-functions"></a>Funciones de incrustación de fuentes

Las siguientes funciones se usan con fuentes OpenType de Microsoft incrustadas.



| Función                                                                   | Descripción                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*\_ALLOCPROC PPC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Función de asignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                              |
| [*\_FREEPROC PPC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Función de desasignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                            |
| [*\_REALLOCPROC PPC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Función de reasignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Crea una versión más compacta de una fuente TrueType especificada para pasarla a una impresora. La fuente resultante puede estar agrupada, comprimida o ambas cosas. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Combina las fuentes de subconjuntos creadas por CreateFontPackage.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Función de devolución de llamada proporcionada por el cliente para leer el contenido de una secuencia desde un búfer.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Convierte una matriz de valores de código de caracteres de 8 bits en valores Unicode de 16 bits.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Libera la memoria usada por una fuente incrustada.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Crea una estructura de fuente que contiene una fuente de carácter ancho agrupado (de 16 bits), utilizando un contexto de dispositivo como origen de la información de incrustación de fuentes.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Crea una estructura de fuente que contiene la fuente de caracteres UCS-4 (32 bits) agrupada, utilizando un contexto de dispositivo como origen de la información de incrustación de fuentes.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Crea una estructura de fuente que contiene una fuente de caracteres anchos (16 bits) agrupada, utilizando un archivo como origen de la información de incrustación de fuentes.                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Agrega o quita facenames de la lista de exclusión de tipo de letra.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Recupera información sobre una fuente incrustada.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Devuelve los privilegios de incrustación de una fuente.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Crea un nuevo nombre para una fuente incrustada instalada.                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Determina si la lista de exclusión de tipos de letra contiene una fuente especificada.                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Determina si la incrustación está habilitada para una fuente especificada.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Lee la fuente incrustada de la secuencia del documento y la instala. También permite que un cliente restrinja aún más los privilegios de incrustación de la fuente.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Valida una parte o todos los datos de glifo de una fuente de caracteres anchos (16 bits) en el intervalo de tamaño especificado.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | Versión UCS-4 de TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Función de devolución de llamada proporcionada por el cliente para escribir el contenido de la secuencia en un búfer.                                                                                  |



 

 

 
