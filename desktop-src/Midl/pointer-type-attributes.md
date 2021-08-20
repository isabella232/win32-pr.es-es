---
title: Atributos de tipo de puntero
description: Los atributos siguientes especifican las características de los punteros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL MIDL, atributos, tipo de puntero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8355a71428c957804596531ea428fb99a779478b677eaa2094cc4db323c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013733"
---
# <a name="pointer-type-attributes"></a>Atributos de tipo de puntero

Los atributos siguientes especifican las características de los punteros.



| Atributo                                   | Uso                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ptr**](ptr.md)                          | Designa un puntero como puntero completo, con todas las funcionalidades de un puntero de lenguaje C, incluidos los alias.                                                                                       |
| [**ref**](ref.md)                          | Designa el tipo más sencillo de puntero en MIDL, que simplemente proporciona la dirección de algunos datos. Los punteros de referencia nunca pueden ser NULL.                                                             |
| [**Único**](unique.md)                    | Permite que un puntero sea NULL, pero no admite alias.                                                                                                                                               |
| [**valor \_ predeterminado del puntero**](pointer-default.md) | Se aplica a una interfaz para especificar el tipo de puntero predeterminado para todos los punteros de esa interfaz, excepto para los punteros de parámetro de nivel superior, que automáticamente tienen como valor predeterminado punteros [**ref.**](ref.md) |
| [**iid \_ es**](iid-is.md)                   | Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.                                                                                                            |
| [**Cadena**](string.md)                    | Especifica que el puntero apunta a una cadena.                                                                                                                                                       |



 

 

 




