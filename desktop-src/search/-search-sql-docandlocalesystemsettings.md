---
description: Cuando el sistema operativo, o incluso una aplicación, se establece para usar un idioma y una configuración regional determinados, muchas configuraciones se ven afectadas.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Documentación y configuración regional del sistema Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed43ae52d7626b759563069b05fe4ae03649feb63fd1af8dab1b80cfd4d558a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594785"
---
# <a name="document-and-system-locale-settings"></a>Documentación y configuración regional del sistema Configuración

Cuando el sistema operativo, o incluso una aplicación, se establece para usar un idioma y una configuración regional determinados, muchas configuraciones se ven afectadas. Estas opciones incluyen formato numérico, formato de fecha, formato de moneda, asignación en mayúsculas y minúsculas, ordenación de diccionarios, tokenización, etc. Aunque esta configuración ayuda a Windows Search proporciona una compatibilidad localizada excelente, pueden producirse resultados inesperados cuando se buscan documentos de una configuración regional mediante un sistema establecido en otra configuración regional.

Cuando el [**objeto IFilter**](/windows/win32/api/filter/nn-filter-ifilter) procesa las propiedades de texto y el contenido de un documento, notifica el idioma de ese documento al indexador de contenido. Con esta información, Windows Search puede aplicar el separador de palabras adecuado.

 

 
