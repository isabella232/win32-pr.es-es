---
description: El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK del instalador de Windows como el archivo Tutorial.cpp.
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: Creación de la acción personalizada Launch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536f22c95d871ab502518a0619efad5ae70cb348cdf75163fc50309b440f6393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045284"
---
# <a name="authoring-the-launch-custom-action"></a>Creación de la acción personalizada Launch

El código fuente de una acción personalizada de ejemplo denominada Launch, que cumple las especificaciones de ejemplo, se proporciona mediante el SDK del instalador de Windows como el archivo Tutorial.cpp. Esta acción personalizada usa [**MsiFormatRecord para**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) dar formato a una cadena que contiene propiedades. La propiedad \[ \# FileKey \] se resuelve en la ruta de acceso completa del archivo HTML. Use el archivo de código fuente para crear el archivo Tutorial.dll. El punto de entrada a este archivo DLL es LaunchTutorial.

La acción personalizada de ejemplo Launch llama a un archivo DLL escrito en C++ y se genera a partir de una secuencia binaria temporal. Las acciones personalizadas de este tipo incluyen las constantes de tipo base msidbCustomActionTypeDll y msidbCustomActionTypeBinaryData, que dan un tipo numérico base igual a 1. Vea Custom Action Type 1 (Tipo [de acción personalizada 1).](custom-action-type-1.md) Dado que las especificaciones requieren que la instalación continúe si se produce un error en la acción personalizada, Launch también incluye la constante **opcional msidbCustomActionTypeContinue**, que es 64. Vea Custom Action Return Processing Options ( Opciones de [procesamiento de devolución de acciones personalizadas).](custom-action-return-processing-options.md) El tipo numérico total de Launch es 65.

Continúe con [Agregar inicio a las tablas CustomAction y Binary](adding-launch-to-the-customaction-and-binary-tables.md).

 

 



