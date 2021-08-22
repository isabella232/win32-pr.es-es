---
description: Las siguientes funciones se usan con fuentes Microsoft OpenType incrustadas.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Funciones de incrustación de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe820c8b9e6a17f148705599d77ea08bbc4b3f8d52821c171c9e86ca13e2ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761188"
---
# <a name="font-embedding-functions"></a>Funciones de incrustación de fuentes

Las siguientes funciones se usan con fuentes Microsoft OpenType incrustadas.



| Función                                                                   | Descripción                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CFP \_ ALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Función de asignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                              |
| [*CFP \_ FREEPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Función de desasignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                            |
| [*CFP \_ REALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Función de reasignación de memoria proporcionada por la aplicación para CreateFontPackage y MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Crea una versión más compacta de una fuente TrueType especificada para pasarla a una impresora. La fuente resultante puede estar en subconjuntos, comprimida o ambas. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Combina fuentes de subconjunto creadas por CreateFontPackage.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Función de devolución de llamada proporcionada por el cliente para leer el contenido de la secuencia desde un búfer.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Convierte una matriz de valores de código de caracteres de 8 bits en valores Unicode de 16 bits.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Libera la memoria usada por una fuente incrustada.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Crea una estructura de fuentes que contiene una fuente de caracteres anchos subconjuntos (16 bits), usando un contexto de dispositivo como origen de información de inserción de fuentes.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Crea una estructura de fuente que contiene la fuente de caracteres UCS-4 subconjuntos (32 bits), usando un contexto de dispositivo como origen de información de inserción de fuentes.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Crea una estructura de fuente que contiene una fuente de caracteres anchos (16 bits) subconjunto, utilizando un archivo como origen de información de inserción de fuentes.                     |
| [**TTEnableEprecioForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Agrega o quita facenames de la lista de exclusión de tipo de letra.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Recupera información sobre una fuente incrustada.                                                                                                            |
| [**TTGetEneotipo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Devuelve los privilegios de inserción de una fuente.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Crea un nuevo nombre para una fuente incrustada instalada.                                                                                                       |
| [**TTIsE kpienabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Determina si la lista de exclusión de tipo de letra contiene una fuente especificada.                                                                                     |
| [**TTIsE kpienabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Determina si la inserción está habilitada para una fuente especificada.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Lee la fuente incrustada de la secuencia de documentos y la instala. También permite a un cliente restringir aún más los privilegios de inserción de la fuente.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Valida parte o todos los datos de glifo de una fuente de caracteres anchos (16 bits), en el intervalo de tamaño especificado.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | Versión UCS-4 de TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Función de devolución de llamada proporcionada por el cliente para escribir el contenido de la secuencia en un búfer.                                                                                  |



 

 

 
