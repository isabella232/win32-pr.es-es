---
title: Agregar una reserva
description: La base de datos de enrutamiento contiene la lista de reservas.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac683c48748fa0e644f2f7569590b3783c521f1d10a1a5852a638a29731daf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014953"
---
# <a name="adding-a-reservation"></a>Agregar una reserva

La base de datos de enrutamiento contiene la lista de reservas. La lista de reservas consta de los usuarios a los que se permite el acceso al espacio de nombres, así como el nivel de acceso para cada usuario que aparece en la reserva. Cuando se agregan o eliminan reservas, se busca en la base de datos de enrutamiento para determinar los privilegios de acceso.

Además de comprobar el identificador de los usuarios, la API del servidor HTTP también comprueba si hay conflictos en las reservas existentes antes de instalar una nueva reserva.

**Para agregar una nueva reserva**

1.  Si el número de puerto de UrlPrefix tiene reservas o registros para un esquema diferente del esquema de UrlPrefix, se produce un error en el registro. HTTP y HTTPS no se admiten en el mismo puerto.
2.  Busque el cubo adecuado para el registro (consulte la sección [Solicitudes entrantes](routing-incoming-requests.md) de enrutamiento), en función del tipo de host. Los pasos restantes son relativos a este cubo.
3.  Seleccione entradas de reserva con componentes de esquema, host y puerto que coincidan con la urlPrefix que se va a reservar. A partir de estos, busque la entrada con el *relativeUri* correspondiente más largo que no sea igual a relativeUri en la reserva (es decir, el *nodo primario*). Si la entrada existe, evalúe los derechos de acceso en función de la ACL asignada a esa entrada.
4.  Si no se encontró un nodo primario, se trata de una reserva con un relativeUri vacío o *una reserva raíz*. Conceda derechos de acceso solo si el autor de la llamada está registrado en las cuentas LocalSystem o Administrator.
5.  Si se conceden derechos de acceso, compruebe si hay reservas duplicadas. Si existe una entrada de reserva con el mismo esquema, puerto, host y relativeUri, se devuelve un código ERROR \_ ALREADY \_ EXISTS.
    > [!Note]  
    > La actualización de una entrada existente debe realizarse en dos pasos: eliminar la entrada y agregar una nueva.

     

Si los pasos anteriores se completan correctamente, se introduce una nueva entrada de reserva en la base de datos de reserva.

> [!Note]  
> La nueva entrada se crea con la ACL especificada y no hereda las ACL de la *entrada* primaria.

 

En los ejemplos siguientes se muestra el proceso de reserva.

-   Reserva 1: el administrador del usuario A y el usuario C se realiza correctamente y `https://+:80/vroot/subdir/` se introduce en el cubo "+".
-   Reserva 2: el administrador del usuario B se realiza correctamente y se especifica en el cubo `https://adatum.com:80/vroot/` "Host explícito".
-   Reserva 3: `https://adatum.com:80/vroot/subdir/otherdir/` por usuario B para el usuario C se realiza correctamente debido a la reserva 2.
-   Reserva 4: `https://+:80/vroot/subdir/otherdir/` el usuario A para el usuario E se realiza correctamente debido a la reserva 1.
-   Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` se produce un error en el usuario A para el usuario E. Acceso denegado debido a la reserva 2.
-   Reserva 6: el `https://+:80/vroot/subdir/` administrador del usuario A produce un error. La reserva entra en conflicto con la reserva 1.
-   Reserva 7: `https://adatum.com:80/newroot/` se produce un error en el usuario A para el usuario A. Acceso denegado debido a la reserva raíz implícita `https://adatum.com:80/` de para LocalSystem o Administrator.

Las reservas pueden afectar al conjunto de direcciones URL de las solicitudes entregadas a un proceso que ha registrado previamente una urlPrefix. Por ejemplo, tenga en cuenta el siguiente caso.

-   Registro: `https://adatum.com:80/vroot/` por aplicación 1 para el usuario A.
-   Se entrega una `https://adatum.com:80/vroot/subdir/file.htm` solicitud de a la aplicación 1.
-   Reserva: `https://+:80/vroot/subdir/` para el usuario B.
-   Ahora se rechaza `https://adatum.com:80/vroot/subdir/file.htm` una solicitud de .
-   Registro: `https://adatum.com:80/vroot/subdir/` por aplicación 2 para el usuario B.
-   Se entrega una `https://adatum.com:80/vroot/subdir/file.htm` solicitud de a la aplicación 2.

 

 




