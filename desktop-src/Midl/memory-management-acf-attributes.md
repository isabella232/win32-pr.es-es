---
title: Atributos ACF de administración de memoria
description: Los atributos enumerados en la tabla siguiente permiten realizar la administración de memoria desde el lado cliente.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- MIDL de ACF, atributos, administración de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159499"
---
# <a name="memory-management-acf-attributes"></a>Atributos ACF de administración de memoria

Los atributos enumerados en la tabla siguiente permiten realizar la administración de memoria desde el lado cliente.



| Atributo                                   | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**allocate**](allocate.md)                | Especifica la manera en que la aplicación cliente y el código auxiliar asignan y liberan memoria para los punteros. Este atributo es especialmente útil cuando se desea que determinadas estructuras de puntero permanezcan accesibles para la aplicación de servidor después de que la llamada al procedimiento remoto vuelva al cliente. También puede usar el atributo [**allocate**](allocate.md) para dirigir el código auxiliar para calcular el tamaño de toda la memoria a la que se hace referencia a través del puntero del tipo especificado y para realizar una sola llamada al usuario [**midl \_ \_ asigna**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**recuento de \_ bytes**](byte-count.md)           | Permite crear un bloque de memoria persistente y contiguo que se puede reutilizar en varias llamadas a procedimiento remoto. Esto libera a la aplicación cliente de la sobrecarga de asignar y liberar memoria repetidamente que puede incluir varios punteros y otras estructuras de datos complejas.                                                                                                                                                                                                                                                      |
| [**habilitar \_ asignación**](enable-allocate.md) | Especifica que el código auxiliar del servidor debe habilitar el entorno de administración de memoria de código auxiliar.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 