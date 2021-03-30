---
description: Una regla de negocio permite a una aplicación usar la lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Reglas de negocios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279636"
---
# <a name="business-rules"></a>Reglas de negocios

Una regla de negocio permite a una aplicación usar la lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.

Una regla de negocios es un script escrito en el lenguaje de programación de Visual Basic Scripting Edition (VBScript) o escrito mediante el software de desarrollo de Microsoft JScript que está asociado a un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Cuando una aplicación comprueba el acceso para una operación, el administrador de autorización comprueba primero si el cliente actual tiene acceso a las tareas que contienen esa operación pero que no están asociadas con las reglas de negocios. Si no se concede el acceso de esta manera, el administrador de autorización ejecuta scripts de reglas de negocios asociados a cualquier tarea que contenga la operación.

Una aplicación pasa información a un script de regla de negocio como un par de matrices que representan los nombres y valores de los parámetros. El script tiene acceso a estos parámetros a través de un objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que se crea cuando se ejecuta el script.

Un script de regla de negocio no se puede asignar a una tarea contenida por un ámbito delegado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Calificar el acceso con la lógica de negocios en C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



