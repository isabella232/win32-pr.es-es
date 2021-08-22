---
description: Dado que el propio archivo DLL de Winsock ya no lo proporciona cada proveedor de pila individual, no es posible que un proveedor de pila ofrezca una funcionalidad ampliada mediante la adición de puntos de entrada al archivo DLL de Winsock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Mecanismo de extensión de función en spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2e5e32a4d79174893cfb2d9fa2ae0c0521a51ac80c40bcb6c45feab49693d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132428"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Mecanismo de extensión de función en spi

Dado que el propio archivo DLL de Winsock ya no lo proporciona cada proveedor de pila individual, no es posible que un proveedor de pila ofrezca una funcionalidad ampliada mediante la adición de puntos de entrada al archivo DLL de Winsock. Para superar esta limitación, Winsock aprovecha la nueva función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para dar cabida a los proveedores de servicios que desean ofrecer extensiones de funcionalidad específicas del proveedor. Este mecanismo presupone que una aplicación es consciente de una extensión determinada y entiende la semántica y la sintaxis implicadas. Esta información la proporcionaría normalmente el proveedor del proveedor de servicios.

Para invocar una función de extensión, la aplicación primero debe solicitar un puntero a la función deseada. Esto se realiza a través de la [**función WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mediante el código de comando SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER. El búfer de entrada de la **función WSAIoctl** contiene un identificador para la función de extensión deseada y el búfer de salida contendrá el propio puntero de función. A continuación, la aplicación puede invocar la función de extensión directamente sin pasar a través de la32.dll \_ Ws2.

Los identificadores asignados a las funciones de extensión son identificadores únicos globales (GUID) asignados por proveedores de servicios. Los proveedores que crean funciones de extensión están invitados a publicar detalles completos sobre la función, incluida la sintaxis del prototipo de función. Esto facilita las funciones de extensión comunes o populares que ofrecen varios proveedores de servicios. Una aplicación puede obtener el puntero de función y usar la función sin necesidad de saber nada sobre el proveedor de servicios concreto que implementa la función.

 

 



