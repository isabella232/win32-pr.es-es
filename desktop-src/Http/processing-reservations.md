---
title: Procesar reservas
description: El administrador del sistema realiza las reservas de partes del espacio de nombres de la dirección URL y se colocan en el almacén de reserva persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421587"
---
# <a name="processing-reservations"></a>Procesar reservas

El administrador del sistema realiza las reservas de partes del espacio de nombres de la dirección URL y se colocan en el almacén de reserva persistente. La raíz del espacio de nombres de la dirección URL para HTTP es propiedad del administrador del sistema. En todos los valores de host y puerto, siempre se asumen las dos reservas siguientes en la raíz del espacio de nombres **relativeUri** .



| Espacio de nombres reservado                 | Reservado para              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Administrador de LocalSystem |
| https:// <host> :<port>/ | Administrador de LocalSystem |



 

Estas reservas implícitas no se pueden quitar. Sin embargo, es posible delegar reservas de raíz explícitas a otros usuarios. Las reservas como las siguientes crearían estas delegaciones:



| Espacio de nombres reservado        | Reservado para |
|---------------------------|--------------|
| `https://+:80/`           | UsuarioA, Usuarioc |
| `https://adatum.com:443/` | UserB        |



 

Si el administrador del sistema quita estas reservas delegadas, la propiedad del espacio de nombres se revierte a la reserva implícita para los valores de puerto y host correspondientes.

 

 




