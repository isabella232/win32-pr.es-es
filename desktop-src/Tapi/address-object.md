---
description: El objeto Address representa una entidad que puede realizar o recibir llamadas.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Objeto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911233"
---
# <a name="address-object"></a>Objeto Address

El objeto Address representa una entidad que puede realizar o recibir llamadas. Este objeto expone interfaces y métodos que permiten a una aplicación realizar una serie de operaciones, como:

-   Detecta si una dirección especificada puede admitir un conjunto determinado de necesidades de tipos de medios.
-   Enumerar las llamadas asociadas actualmente a la dirección.
-   Crear o reenviar llamadas.
-   Obtiene el nombre del proveedor de servicios asociado.
-   Si existe un proveedor de servicios multimedia, obtenga punteros de interfaz que permitan la manipulación detallada del terminal.
-   Obtiene y establece otra información, como si un mensaje está en espera.

La mayoría de las direcciones están asociadas a un terminal, pero no es el caso de forma uniforme. Por ejemplo, un TSP remoto que proporciona acceso al equipo en un servidor tendrá una dirección en el equipo local, pero no un terminal. Un módem sin altavoz tampoco tiene ningún terminal asociado a su dirección.

Si una dirección no tiene un terminal asociado, la interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) no se expone en el objeto.

En el ejemplo de código [seleccionar una dirección](select-an-address.md) se muestra el proceso básico para adquirir un puntero de objeto de dirección.

Vea [interfaces del objeto Address](address-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto Address.

 

 
