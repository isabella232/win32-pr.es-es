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
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="23605-103">Configuración regional del sistema y del documento</span><span class="sxs-lookup"><span data-stu-id="23605-103">Document and System Locale Settings</span></span>

<span data-ttu-id="23605-104">Cuando el sistema operativo, o incluso una aplicación, está configurado para usar un idioma y una configuración regional determinados, se ven afectados muchos valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="23605-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="23605-105">Estas opciones incluyen el formato numérico, el formato de fecha, el formato de moneda, la asignación en mayúsculas y minúsculas, el orden de ordenación del diccionario, la tokenización y otros.</span><span class="sxs-lookup"><span data-stu-id="23605-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="23605-106">Aunque esta configuración ayuda a la búsqueda de Windows a proporcionar una excelente compatibilidad localizada, pueden producirse resultados inesperados cuando se buscan documentos de una configuración regional mediante un sistema que está establecido en otra configuración regional.</span><span class="sxs-lookup"><span data-stu-id="23605-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="23605-107">Cuando el objeto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) procesa el contenido y las propiedades de texto de un documento, informa del idioma de dicho documento al indizador de contenido.</span><span class="sxs-lookup"><span data-stu-id="23605-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="23605-108">Con esta información, Windows Search puede aplicar el separador de palabras adecuado.</span><span class="sxs-lookup"><span data-stu-id="23605-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
