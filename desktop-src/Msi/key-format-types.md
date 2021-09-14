---
description: Los tipos de formato de clave de datos configurables se pueden usar en campos de texto para proporcionar una clave en una tabla de base de datos.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipos de formato de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071995"
---
# <a name="key-format-types"></a>Tipos de formato de clave

Los tipos de formato de clave de datos configurables se pueden usar en campos de texto para proporcionar una clave en una tabla de base de datos. El atributo msmConfigItemNonNullable está implícito en este formato de datos y no es necesario establecerlo. Null nunca es un valor válido para este tipo. Las respuestas a todos los elementos de formato clave deben estar en formato especial [de CMSM.](cmsm-special-format.md)

Existen los siguientes tipos de formato de clave:

[Tipo de directorio](directory-type.md)

[Tipo de archivo](file-type.md)

[Tipo de propiedad](property-type.md)

[Tipo de diálogo](dialog-type.md)

[Tipo binario](binary-type.md)

[Tipo de icono](icon-type.md)

Los elementos configurables del tipo de formato de clave se usan en columnas de texto para proporcionar una clave de base de datos y, en general, podrían reemplazarse por cualquier cadena de texto. Los tipos individuales pueden tener restricciones sintácticas adicionales, pero estas restricciones no se aplican Mergemod.dll. Determinados elementos configurables también pueden tener restricciones semánticas de características. Por ejemplo, puede ser necesario que un elemento configurable determinado sea una clave de la [tabla Binaria](binary-table.md) para una fila que contenga una imagen de mapa de bits. Estas restricciones no se aplican mediante Mergemod.dll, por lo que los autores de módulos deben estar preparados para controlar cualquier cadena que cumpla el tipo de formato de clave especificado. A menos que se especifique lo contrario por significado semántico o atributos, null es una respuesta válida.

 

 



