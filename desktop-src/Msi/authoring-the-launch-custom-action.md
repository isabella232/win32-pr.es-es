---
description: El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK de Windows Installer como archivo tutorial. cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Crear la acción personalizada iniciar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001721"
---
# <a name="authoring-the-launch-custom-action"></a>Crear la acción personalizada iniciar

El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK de Windows Installer como archivo tutorial. cpp. Esta acción personalizada usa [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para dar formato a una cadena que contiene propiedades. La propiedad \[ \# FileKey \] se resuelve en la ruta de acceso completa del archivo HTML. Use el archivo de origen para crear el Tutorial.dll de archivo. El punto de entrada a este archivo DLL es LaunchTutorial.

El inicio de la acción personalizada de ejemplo llama a un archivo DLL escrito en C++ y se genera a partir de una secuencia binaria temporal. Entre las acciones personalizadas de este tipo se incluyen las constantes de tipo base msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData, que dan un tipo numérico base igual a 1. Consulte [acción personalizada tipo 1](custom-action-type-1.md). Dado que las especificaciones requieren que la instalación continúe si se produce un error en la acción personalizada, el lanzamiento también incluye la constante opcional **msidbCustomActionTypeContinue**, que es 64. Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md). El tipo numérico total de Launch es 65.

Continúe [agregando el inicio a las tablas de CustomAction y binarias](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



