---
title: Procesamiento de registros
description: Las API de servidor HTTP utilizan la base de datos de enrutamiento para aplicar comprobaciones de acceso durante los registros.
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e02d2511d9967454d5cbddd93b2c0380d1172
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488500"
---
# <a name="processing-registrations"></a>Procesamiento de registros

Las API de servidor HTTP utilizan la base de datos de enrutamiento para aplicar comprobaciones de acceso durante los registros. Un registro para un [UrlPrefix](urlprefix-strings.md) debe pasar una serie de comprobaciones de acceso para asegurarse de que el usuario que se registra para el espacio de nombres tiene derechos de acceso. Utilice la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) para agregar un nuevo registro.

**Para agregar un nuevo registro con HttpAddUrl**

1.  Si el número de puerto de UrlPrefix tiene reservas o registros para un esquema diferente del esquema en el UrlPrefix, se produce un error en el registro. HTTP y HTTPS no se admiten en el mismo puerto.
2.  El registro se divide en el depósito adecuado para el registro. Los cubos se basan en el tipo de host de la dirección URL, tal como se describe en la sección [enrutamiento de solicitudes entrantes](routing-incoming-requests.md) . Los pasos siguientes son relativos a este depósito en particular.
3.  Si existe una entrada de registro duplicada, devuelve un código de error.
4.  Seleccione las entradas de reserva con los componentes de esquema, host y puerto que son iguales a los de UrlPrefix. A partir de estos, busque la entrada con la coincidencia de **relativeUri** más larga. Si la entrada existe, compruebe los permisos en función de la ACL asociada a esa entrada y devuelva el resultado correcto. Si la entrada no existe, la devolución de un ERROR \_ ya existe en el \_ código.

En los siguientes ejemplos se muestra el proceso para instalar un registro en la base de datos de enrutamiento. Las reservas 1 y 2 existen en la base de datos de enrutamiento.

-   Reserva 1: `https://+:80/vroot/subdir/` para el usuario a y el usuario C. Esta reserva se coloca en el cubo "+".
-   Reserva 2: `https://adatum.com:80/vroot/` para el usuario B. Esta reserva se coloca en el cubo "host explícito".
-   Registro: el `https://+:80/vroot/subdir/` usuario B produce un error debido a la reserva 1.
-   Registro: el `https://adatum.com:80/vroot/subdir/` usuario B se ejecuta correctamente debido a la reserva 2.
-   Registro: `https://adatum.com:80/vroot/subdir/` el usuario C produce un error debido a la reserva más explícita 2. La reserva de caracteres comodín seguros no tiene significado en el contexto de la reserva o registro explícitos.
-   Registro: `https://+:80/vroot/subdir/` el usuario a se realiza correctamente debido A la reserva 1.
-   Registro: el `https://adatum.com:80/vroot/anotherdir/` usuario B se ejecuta correctamente debido a la reserva 2.

La comprobación de acceso para el registro no incluye comprobaciones de privilegios de delegación. No hay comprobaciones de acceso basadas en las reservas (vea [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)). El único requisito para eliminar un registro nos indica que el proceso de llamada debe haber creado el registro.

 

 




