---
title: Procesamiento de registros
description: Las API del servidor HTTP usan la base de datos de enrutamiento para aplicar comprobaciones de acceso durante los registros.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393848"
---
# <a name="processing-registrations"></a>Procesamiento de registros

Las API del servidor HTTP usan la base de datos de enrutamiento para aplicar comprobaciones de acceso durante los registros. Un registro de [UrlPrefix](urlprefix-strings.md) debe pasar una serie de comprobaciones de acceso para asegurarse de que el usuario que se registra para el espacio de nombres tiene derechos de acceso. Use la [**función HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para agregar un nuevo registro.

**Para agregar un nuevo registro con HttpAddUrl**

1.  Si el número de puerto de UrlPrefix tiene reservas o registros para un esquema diferente del esquema de UrlPrefix, se produce un error en el registro. HTTP y HTTPS no se admiten en el mismo puerto.
2.  El registro se divide en el depósito adecuado para el registro. Los depósitos se basan en el tipo de host de la dirección URL, como se describe en la sección [Solicitudes entrantes de](routing-incoming-requests.md) enrutamiento. Los pasos siguientes son relativos a este cubo concreto.
3.  Si existe una entrada de registro duplicada, devuelva un código de error.
4.  Seleccione entradas de reserva con componentes de esquema, host y puerto que sean iguales a los de UrlPrefix. Desde estos, busque la entrada con la coincidencia **relativeUri más** larga. Si la entrada existe, compruebe los permisos en función de la ACL asociada a esa entrada y devuelva correcto. Si la entrada no existe, devuelva un código ERROR \_ ALREADY \_ EXISTS.

En los ejemplos siguientes se muestra el proceso para instalar un registro en la base de datos de enrutamiento. Las reservas 1 y 2 existen en la base de datos de enrutamiento.

-   Reserva 1: `https://+:80/vroot/subdir/` para el usuario A y el usuario C. Esta reserva se coloca en el cubo "+".
-   Reserva 2: `https://adatum.com:80/vroot/` para el usuario B. Esta reserva se coloca en el cubo "Host explícito".
-   Registro: `https://+:80/vroot/subdir/` el usuario B produce un error debido a la reserva 1.
-   Registro: `https://adatum.com:80/vroot/subdir/` el usuario B se realiza correctamente debido a la reserva 2.
-   Registro: `https://adatum.com:80/vroot/subdir/` el usuario C produce un error debido a la reserva 2 más explícita. La reserva de caracteres comodín segura no tiene significado en el contexto de la reserva o el registro explícitos.
-   Registro: `https://+:80/vroot/subdir/` el usuario A se realiza correctamente debido a la reserva 1.
-   Registro: `https://adatum.com:80/vroot/anotherdir/` el usuario B se realiza correctamente debido a la reserva 2.

La comprobación de acceso para el registro no incluye comprobaciones de privilegios de delegación. No hay comprobaciones de acceso basadas en reservas [**(vea HttpRemoveUrl).**](/windows/desktop/api/Http/nf-http-httpremoveurl) El único requisito para eliminar un registro es que el proceso de llamada debe haber creado el registro.

 

 




