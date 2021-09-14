---
description: El tipo de identificador de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074453"
---
# <a name="identifier-type"></a>Tipo de identificador

El tipo de identificador de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto proporcionada por el usuario en el formato de un identificador Windows [instalador](identifier.md). La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato, escribir "Identificador" en la columna Tipo y dejar en blanco la columna ContextData de la tabla [ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier idioma compatible con la página de códigos de la base de datos. Vea [Control de páginas de códigos (Windows Installer).](code-page-handling-windows-installer-.md) Null es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



