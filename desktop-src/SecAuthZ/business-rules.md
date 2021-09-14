---
description: Una regla de negocios permite que una aplicación use lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Reglas de negocios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160857"
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

 

 



