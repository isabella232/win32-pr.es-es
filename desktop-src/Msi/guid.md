---
description: El tipo de datos GUID es una cadena de texto que representa un identificador de clase (ID). COM debe poder convertir la cadena en un identificador de clase válido. Todos los GUID deben crearse en mayúsculas.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074721"
---
# <a name="guid"></a>GUID

El tipo de datos GUID es una cadena de texto que representa un identificador de clase (ID). COM debe poder convertir la cadena en un identificador de clase válido. Todos los GUID deben crearse en mayúsculas.

El formato válido para un GUID es {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} donde X es un dígito hexadecimal (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).

Tenga en cuenta que utilidades como GUIDGEN pueden generar GUID que contengan letras minúsculas. Todos estos deben cambiarse a letras mayúsculas antes de que el instalador pueda usar el GUID como código de producto, código de paquete o código de componente válido.

 

 



