---
description: Una página de códigos es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de caracteres.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Comprobar la página de códigos de la base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedb63128d4a3b18878eba16af5e55da92403953ddf2a2c9a29c788a524ad41f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581775"
---
# <a name="checking-the-installation-database-code-page"></a>Comprobar la página de códigos de la base de datos de instalación

Una *página de códigos* es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de caracteres. Las distintas páginas de códigos proporcionan compatibilidad con los juegos de caracteres que se usan en distintos países o regiones. Las páginas de códigos se conocen por número; Por ejemplo, la página de códigos 932 representa el juego de caracteres japonés y la página de códigos 950 representa uno de los juegos de caracteres en chino. Vea [Localización de las tablas Error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos ASCII.

La misma página de códigos ASCII, 1252, se puede usar para inglés y francés. Por lo tanto, no es necesario restablecer la página de códigos MNP2000.msi base de datos (inglés) para cambiar la instalación a francés.

Para obtener más información sobre cómo establecer la página de códigos, vea Control de páginas de [códigos (Windows Instalador).](code-page-handling-windows-installer-.md)

[Continuar](importing-localized-error-and-actiontext-tables.md)

 

 



