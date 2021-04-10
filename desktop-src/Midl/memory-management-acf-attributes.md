---
title: Atributos ACF de administración de memoria
description: Los atributos que se enumeran en la tabla siguiente permiten realizar la administración de la memoria desde el lado cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF (MIDL), atributos, administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995200"
---
# <a name="memory-management-acf-attributes"></a>Atributos ACF de administración de memoria

Los atributos que se enumeran en la tabla siguiente permiten realizar la administración de la memoria desde el lado cliente.



| Atributo                                   | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**allocate**](allocate.md)                | Especifica el modo en que la aplicación cliente y el código auxiliar asignan y liberan memoria para los punteros. Este atributo es especialmente útil cuando se desea que ciertas estructuras de puntero sigan siendo accesibles para la aplicación de servidor después de que la llamada a procedimiento remoto se devuelva al cliente. También puede usar el atributo [**allocate**](allocate.md) para dirigir el código auxiliar para calcular el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y para hacer una llamada única a la [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**recuento de bytes \_**](byte-count.md)           | Permite crear un bloque persistente y contiguo de memoria que se puede reutilizar en varias llamadas a procedimientos remotos. Esto libera la aplicación cliente de la sobrecarga de la asignación y liberación repetidas de memoria que pueden incluir varios punteros y otras estructuras de datos complejas.                                                                                                                                                                                                                                                      |
| [**habilitar \_ asignación**](enable-allocate.md) | Especifica que el código auxiliar de servidor debe habilitar el entorno de administración de memoria de código auxiliar.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 