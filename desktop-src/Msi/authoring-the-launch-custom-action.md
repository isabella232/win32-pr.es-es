---
description: El SDK del instalador de Windows proporciona el código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, como el archivo Tutorial.cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Creación de la acción personalizada Launch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159009"
---
# <a name="authoring-the-launch-custom-action"></a>Creación de la acción personalizada Launch

El SDK del instalador de Windows proporciona el código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, como el archivo Tutorial.cpp. Esta acción personalizada usa [**MsiFormatRecord para**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) dar formato a una cadena que contiene propiedades. La propiedad \[ \# FileKey \] se resuelve en la ruta de acceso completa del archivo HTML. Use el archivo de origen para crear el archivo Tutorial.dll. El punto de entrada a este archivo DLL es LaunchTutorial.

La acción personalizada de ejemplo Launch llama a un archivo DLL escrito en C++ y se genera a partir de una secuencia binaria temporal. Las acciones personalizadas de este tipo incluyen las constantes de tipo base msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData, que dan un tipo numérico base igual a 1. Vea Custom Action Type 1 ( Tipo [de acción personalizada 1).](custom-action-type-1.md) Dado que las especificaciones requieren que la instalación continúe si se produce un error en la acción personalizada, Launch también incluye la constante **opcional msidbCustomActionTypeContinue**, que es 64. Vea [Opciones de procesamiento de devolución de acciones personalizadas.](custom-action-return-processing-options.md) El tipo numérico total de Launch es 65.

Continúe con Adding Launch to the CustomAction and Binary Tables (Agregar inicio [a las tablas CustomAction y Binary).](adding-launch-to-the-customaction-and-binary-tables.md)

 

 



