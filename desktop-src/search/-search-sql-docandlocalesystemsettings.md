---
description: Cuando el sistema operativo, o incluso una aplicación, está configurado para usar un idioma y una configuración regional determinados, se ven afectados muchos valores de configuración.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Configuración regional del sistema y del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715004"
---
# <a name="document-and-system-locale-settings"></a>Configuración regional del sistema y del documento

Cuando el sistema operativo, o incluso una aplicación, está configurado para usar un idioma y una configuración regional determinados, se ven afectados muchos valores de configuración. Estas opciones incluyen el formato numérico, el formato de fecha, el formato de moneda, la asignación en mayúsculas y minúsculas, el orden de ordenación del diccionario, la tokenización y otros. Aunque esta configuración ayuda a la búsqueda de Windows a proporcionar una excelente compatibilidad localizada, pueden producirse resultados inesperados cuando se buscan documentos de una configuración regional mediante un sistema que está establecido en otra configuración regional.

Cuando el objeto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) procesa el contenido y las propiedades de texto de un documento, informa del idioma de dicho documento al indizador de contenido. Con esta información, Windows Search puede aplicar el separador de palabras adecuado.

 

 
