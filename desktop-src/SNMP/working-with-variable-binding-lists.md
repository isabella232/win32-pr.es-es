---
title: Trabajar con listas de enlaces de variables
description: Un enlace de variable es el emparejamiento de un nombre de instancia de objeto SNMP con un valor asociado. Una lista de enlaces de variables es una serie de entradas de enlace de variables. En WinSNMP, una unidad de datos de protocolo (PDU) incluye una lista de enlace de variables.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Trabajar con listas de enlaces de variables SNMP
- Enlace de variables Enumera SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35abc72501d1b3f93dcc6bf0004f5425e951e299f7948d239888ea010d295252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142727"
---
# <a name="working-with-variable-binding-lists"></a>Trabajar con listas de enlaces de variables

Un *enlace de variable* es el emparejamiento de un nombre de instancia de objeto SNMP con un valor asociado. Una *lista de enlaces de* variables es una serie de entradas de enlace de variables. En WinSNMP, una unidad de datos de protocolo (PDU) incluye una lista de enlace de variables.

Los detalles de la estructura de lista de enlaces de variables están restringidos a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede acceder a una lista de enlaces de variables con un identificador de tipo **HSNMP \_ VBL**. Para obtener más información, vea [Objetos de identificador de recursos.](resource-handle-objects.md)

La aplicación WinSNMP puede construir y manipular listas de enlaces de variables e incluirlas en PDU. Para realizar estas operaciones, la aplicación usa las funciones de enlace [de variables de](winsnmp-functions.md)WinSNMP . Para obtener más información sobre cómo trabajar con WinSNMP y listas de enlaces de variables, vea los temas enumerados en la tabla siguiente.



| Tema                                                                    | Descripción                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [Crear una lista de enlaces de variables](creating-a-variable-binding-list.md) | Describe cómo crear una lista de enlaces de variables. |
| [Administración de una lista de enlaces de variables](managing-a-variable-binding-list.md) | Describe cómo administrar una lista de enlaces de variables. |



 

Para obtener más información sobre los enlaces de variables y las listas de enlaces de variables, vea [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Operaciones de protocolo para la versión 2 del Protocolo simple de administración de redes (SNMPv2)" y las funciones de enlace de [variables](winsnmp-functions.md)de WinSNMP .

 

 




