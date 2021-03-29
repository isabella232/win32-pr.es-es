---
title: Atributos de tipo de puntero
description: Los atributos siguientes especifican las características de los punteros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL, atributos, tipo de puntero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779891"
---
# <a name="pointer-type-attributes"></a>Atributos de tipo de puntero

Los atributos siguientes especifican las características de los punteros.



| Atributo                                   | Uso                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ptr**](ptr.md)                          | Designa un puntero como un puntero completo, con todas las capacidades de un puntero de lenguaje C, incluido el alias.                                                                                       |
| [**ref**](ref.md)                          | Designa el tipo más simple de puntero en MIDL, uno que simplemente proporciona la dirección de algunos datos. Los punteros de referencia nunca pueden ser null.                                                             |
| [**espeficarse**](unique.md)                    | Permite que un puntero sea NULL, pero no admite el alias.                                                                                                                                               |
| [**puntero \_ predeterminado**](pointer-default.md) | Se aplica a una interfaz para especificar el tipo de puntero predeterminado para todos los punteros de la interfaz, excepto para los punteros de parámetros de nivel superior, que automáticamente tienen como valor predeterminado los punteros de [**referencia**](ref.md) . |
| [**IID \_ es**](iid-is.md)                   | Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.                                                                                                            |
| [**string**](string.md)                    | Especifica que el puntero apunta a una cadena.                                                                                                                                                       |



 

 

 




