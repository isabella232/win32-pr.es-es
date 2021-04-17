---
description: Una página de códigos es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de carácter.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Comprobar la página de códigos de la base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666997"
---
# <a name="checking-the-installation-database-code-page"></a>Comprobar la página de códigos de la base de datos de instalación

Una *Página de códigos* es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de carácter. Diferentes páginas de códigos proporcionan compatibilidad con los juegos de caracteres que se usan en diferentes países o regiones. Se hace referencia a las páginas de códigos por número; por ejemplo, la página de códigos 932 representa el juego de caracteres japoneses y la página de códigos 950 representa uno de los juegos de caracteres chinos. Consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos ASCII.

Se puede usar la misma página de códigos ASCII, 1252 para inglés y francés. Por lo tanto, no es necesario restablecer la página de códigos del MNP2000.msi de base de datos (Inglés) para cambiar la instalación a francés.

Para obtener más información sobre cómo establecer la página de códigos [, vea control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md).

[Continuar](importing-localized-error-and-actiontext-tables.md)

 

 



