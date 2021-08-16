---
description: Una regla de negocios permite que una aplicación use lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Reglas de negocios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54260fc6c7dd56137b3065a07f0dcccf9df1c4d21add4b9e7f0cfa79b0300e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783631"
---
# <a name="business-rules"></a>Reglas de negocios

Una regla de negocios permite que una aplicación use lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.

Una regla de negocios es un script escrito en el lenguaje de programación Visual Basic Scripting Edition (VBScript) o escrito con el software de desarrollo de Microsoft JScript asociado a un objeto [**IAzTask.**](/windows/desktop/api/Azroles/nn-azroles-iaztask) Cuando una aplicación comprueba el acceso de una operación, el Administrador de autorización comprueba primero si el cliente actual tiene acceso a las tareas que contienen esa operación pero que no están asociadas a reglas de negocios. Si el acceso no se concede de esta manera, el Administrador de autorización ejecuta scripts de reglas de negocio asociados a cualquier tarea que contenga la operación.

Una aplicación pasa información a un script de regla de negocios como un par de matrices que representan los nombres y valores de los parámetros. El script tiene acceso a estos parámetros a través de [**un objeto AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que se crea cuando se ejecuta el script.

No se puede asignar un script de regla de negocio a una tarea contenida en un ámbito delegado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Calificar el acceso con lógica de negocios en C++](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



