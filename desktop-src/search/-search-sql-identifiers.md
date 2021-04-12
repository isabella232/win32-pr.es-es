---
description: Los identificadores especifican los nombres de las columnas (a veces denominadas propiedades), los catálogos y los alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153957"
---
# <a name="identifiers"></a>Identificadores

Los identificadores especifican los nombres de las columnas (a veces denominadas propiedades), los catálogos y los alias. Por ejemplo, System. ItemName y System. DateCreated son los identificadores de dos columnas de propiedades definidas por el sistema. Por el contrario, los literales especifican valores de cadena y numéricos.


Puede crear identificadores de hasta 128 caracteres de longitud y en uno de dos tipos, que se distinguen por los caracteres que se usan en el nombre del identificador:

-   Los **identificadores normales** solo contienen los caracteres a-z, a-z, 0-9, subrayado ( \_ ) y punto (.), y comienzan por una letra. No es necesario incluir los identificadores normales entre comillas dobles ("").
-   Los **identificadores delimitados** pueden contener cualquier carácter Unicode válido y deben ir entre comillas dobles.

> [!Note]  
> En las cláusulas FREETEXT y Contains, puede utilizar el asterisco ( \* ) como identificador de columna especial si desea especificar que Windows Search incluya todas las propiedades indizadas en la consulta. Aunque no es un identificador normal, no requiere comillas dobles.

 

 

 



