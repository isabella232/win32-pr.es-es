---
description: El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Crear una base de datos con una página de códigos neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082794"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>Crear una base de datos con una página de códigos neutra

El enfoque recomendado para controlar las páginas de códigos es crear una base de datos base neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos. A continuación, la base de datos se puede establecer en la página de códigos de la localización y se puede Agregar la información de localización como se describe en [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md).

Para crear una base de datos neutra, evite los caracteres extendidos que no pertenecen al Juego de caracteres ASCII y, por tanto, requieren una página de códigos especial. Por ejemplo, el signo de copyright, el © y el signo de marca registrada,, no son caracteres ASCII y requieren una página de códigos ANSI especial para la presentación adecuada. En su lugar, use (c) y (r), ya que estos caracteres se pueden traducir o transformar en los símbolos para la versión en inglés. Esta base de datos neutra puede localizarse después configurando su página de códigos y agregando información de localización por edición de tabla o importando archivos de archivo de texto.

 

 



