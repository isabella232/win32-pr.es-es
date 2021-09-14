---
description: El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir a cualquier página de códigos.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Crear una base de datos con una página de códigos neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158738"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Crear una base de datos con una página de códigos neutra

El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir a cualquier página de códigos. A continuación, la base de datos se puede establecer en la página de códigos de la localización y la información de localización se puede agregar como se describe en [Localización](localizing-a-windows-installer-package.md)de un paquete Windows instalador .

Para crear una base de datos neutra, evite los caracteres extendidos que no pertenezcan al juego de caracteres ASCII y, por tanto, requieran una página de códigos especial. Por ejemplo, el signo de copyright, © y el signo de marca comercial registrado, , no son caracteres ASCII y requieren una página de códigos ANSI especial para una presentación adecuada. En su lugar, use (c) y (r), ya que estos caracteres se pueden traducir o transformar en los símbolos de la versión en inglés. Esta base de datos neutra se puede localizar estableciendo su página de códigos y agregando información de localización mediante la edición de tablas o importando archivos de archivo de texto.

 

 



