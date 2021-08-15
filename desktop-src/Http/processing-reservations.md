---
title: Procesamiento de reservas
description: Las reservas de partes del espacio de nombres de dirección URL las realiza el administrador del sistema y se colocan en el almacén de reservas persistente.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f0e38f5994687bfe26d1334300c0aa7fbbd3f8096abcf60e6c523e7d030a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393767"
---
# <a name="processing-reservations"></a>Procesamiento de reservas

Las reservas de partes del espacio de nombres de dirección URL las realiza el administrador del sistema y se colocan en el almacén de reservas persistente. La raíz del espacio de nombres de dirección URL para HTTP es propiedad del administrador del sistema. Para todos los valores de host y puerto, siempre se asumen las dos reservas siguientes en la raíz del espacio **de nombres relativeUri.**



| Espacio de nombres reservado                 | Reservado para              |
|------------------------------------|---------------------------|
| https:// <host> :<port>/  | Administrador del sistema local |
| https:// <host> :<port>/ | Administrador del sistema local |



 

Estas reservas implícitas no se pueden quitar. Sin embargo, es posible delegar reservas raíz explícitas a otros usuarios. Las reservas como las siguientes crearían estas delegaciones:



| Espacio de nombres reservado        | Reservado para |
|---------------------------|--------------|
| `https://+:80/`           | UserA, UserC |
| `https://adatum.com:443/` | UserB        |



 

Si el administrador del sistema quita estas reservas delegadas, la propiedad del espacio de nombres vuelve a la reserva implícita para los valores de host y puerto correspondientes.

 

 




