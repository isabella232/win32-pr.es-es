---
description: Dado que el propio archivo DLL de Winsock ya no lo suministra cada proveedor de pila individual, no es posible que un proveedor de pila ofrezca la funcionalidad extendida mediante la adición de puntos de entrada a la DLL de Winsock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Mecanismo de extensión de función en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cfa6c9dfaf3afcec8e6861a9a0d3545a7ed0c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705621"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Mecanismo de extensión de función en el SPI

Dado que el propio archivo DLL de Winsock ya no lo suministra cada proveedor de pila individual, no es posible que un proveedor de pila ofrezca la funcionalidad extendida mediante la adición de puntos de entrada a la DLL de Winsock. Para superar esta limitación, Winsock aprovecha la nueva función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para dar cabida a los proveedores de servicios que desean ofrecer extensiones de funcionalidad específicas del proveedor. Este mecanismo presupone que una aplicación es consciente de una extensión determinada y entiende la semántica y la sintaxis implicadas. Normalmente, el proveedor de servicios proporciona dicha información.

Para invocar una función de extensión, la aplicación debe solicitar primero un puntero a la función deseada. Esto se realiza a través de la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con el código de comando de la \_ función de extensión SiO Get \_ \_ \_ . El búfer de entrada de la función **WSAIoctl** contiene un identificador para la función de extensión deseada y el búfer de salida contendrá el propio puntero de función. A continuación, la aplicación puede invocar la función de extensión directamente sin pasar por el \_32.dll Ws2.

Los identificadores asignados a las funciones de extensión son identificadores únicos globales (GUID) que se asignan a los proveedores del proveedor de servicios. Se recomienda a los proveedores que creen funciones de extensión que publiquen todos los detalles sobre la función, incluida la sintaxis del prototipo de función. Esto facilita que varios proveedores de servicios ofrezcan funciones de extensión comunes y/o populares. Una aplicación puede obtener el puntero de función y utilizar la función sin necesidad de saber nada sobre el proveedor de servicios concreto que implementa la función.

 

 



