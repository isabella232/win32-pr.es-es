---
description: Una página de códigos es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de caracteres.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Comprobación de la página de códigos de la base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158917"
---
# <a name="checking-the-installation-database-code-page"></a>Comprobación de la página de códigos de la base de datos de instalación

Una *página de códigos* es una tabla interna que el sistema operativo usa para asignar símbolos (letras, números y caracteres de puntuación) a un número de caracteres. Las distintas páginas de códigos proporcionan compatibilidad con los juegos de caracteres usados en distintos países o regiones. Las páginas de códigos se conocen por número; Por ejemplo, la página de códigos 932 representa el juego de caracteres japonés y la página de códigos 950 representa uno de los juegos de caracteres en chino. Vea [Localización de las tablas Error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos ASCII.

La misma página de códigos ASCII, 1252, se puede usar para inglés y francés. Por lo tanto, no es necesario restablecer la página de códigos MNP2000.msi base de datos (inglés) para cambiar la instalación a francés.

Para obtener más información sobre cómo establecer la página de códigos, vea Control de páginas de [códigos (Windows Installer).](code-page-handling-windows-installer-.md)

[Continuar](importing-localized-error-and-actiontext-tables.md)

 

 



