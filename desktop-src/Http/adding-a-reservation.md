---
title: Agregar una reserva
description: La base de datos de enrutamiento contiene la lista de reserva.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104533586"
---
# <a name="adding-a-reservation"></a>Agregar una reserva

La base de datos de enrutamiento contiene la lista de reserva. La lista de reserva consta de los usuarios a los que se permite el acceso al espacio de nombres, así como el nivel de acceso de cada usuario que se muestra en la reserva. Cuando se agregan o eliminan reservas, se busca en la base de datos de enrutamiento para determinar los privilegios de acceso.

Además de comprobar el ID. de usuario, la API del servidor HTTP también comprueba los conflictos en las reservas existentes antes de instalar una nueva reserva.

**Para agregar una nueva reserva**

1.  Si el número de puerto de UrlPrefix tiene reservas o registros para un esquema diferente del esquema en el UrlPrefix, se produce un error en el registro. HTTP y HTTPS no se admiten en el mismo puerto.
2.  Busque el depósito adecuado para el registro (consulte la sección [enrutamiento de solicitudes entrantes](routing-incoming-requests.md) ), en función del tipo de host. Los pasos restantes son relativos a este cubo.
3.  Seleccione las entradas de reserva con los componentes de esquema, host y puerto que coincidan con el UrlPrefix que se va a reservar. A partir de estos, busque la entrada con el valor de *relativeUri* que coincida más largo y que no sea igual a relativeUri en la reserva (es decir, el *nodo primario*). Si la entrada existe, evalúe los derechos de acceso en función de la ACL asignada a esa entrada.
4.  Si no se encuentra un nodo primario, se trata de una reserva con un objeto relativeUri vacío o una *reserva raíz*. Conceda derechos de acceso solo si el autor de la llamada se registra en las cuentas LocalSystem o administrador.
5.  Si se conceden derechos de acceso, compruebe si hay reservas duplicadas. Si existe una entrada de reserva con el mismo esquema, puerto, host y relativeUri, \_ \_ se devuelve un código de error.
    > [!Note]  
    > La actualización de una entrada existente debe realizarse en dos pasos: Elimine la entrada y agregue una nueva.

     

Si los pasos anteriores se realizan correctamente, se introduce una nueva entrada de reserva en la base de datos de reserva.

> [!Note]  
> La nueva entrada se crea con la ACL especificada y no hereda las ACL de la entrada *primaria* .

 

En los siguientes ejemplos se muestra el proceso de reserva.

-   Reserva 1: `https://+:80/vroot/subdir/` por administrador para el usuario a y el usuario C se realiza correctamente y se especifica en el cubo "+".
-   Reserva 2: `https://adatum.com:80/vroot/` por el administrador del usuario B se realiza correctamente y se especifica en el cubo "host explícito".
-   Reserva 3: el `https://adatum.com:80/vroot/subdir/otherdir/` usuario B para el usuario C se realiza correctamente debido a la reserva 2.
-   Reserva 4: `https://+:80/vroot/subdir/otherdir/` por el usuario a para el usuario E se realiza correctamente debido A la reserva 1.
-   Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` por el usuario a para el usuario E produce un error. Acceso denegado debido a la reserva 2.
-   Reserva 6: `https://+:80/vroot/subdir/` el administrador del usuario a produce un error. La reserva entra en conflicto con la reserva 1.
-   Reserva 7: `https://adatum.com:80/newroot/` por el usuario a para el usuario a, se produce un error. Acceso denegado debido a la reserva de raíz implícita de `https://adatum.com:80/` para LocalSystem o administrador.

Las reservas pueden afectar al conjunto de direcciones URL en las solicitudes entregadas a un proceso que ha registrado previamente un UrlPrefix. Por ejemplo, tenga en cuenta el siguiente caso.

-   Registro: `https://adatum.com:80/vroot/` por aplicación 1 para el usuario A.
-   Una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` se entrega a la aplicación 1.
-   Reserva: `https://+:80/vroot/subdir/` para el usuario B.
-   Ahora se ha rechazado una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` .
-   Registro: `https://adatum.com:80/vroot/subdir/` por aplicación 2 para el usuario B.
-   Una solicitud de `https://adatum.com:80/vroot/subdir/file.htm` se entrega a la aplicación 2.

 

 




