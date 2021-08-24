---
title: add urlacl
description: Reserva la dirección URL especificada para usuarios y cuentas que no son administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- add urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: e3f4c715df70255ede8bd9ca5fc23131102983f8a3aeeb25735d5fc81d5ad9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638785"
---
# <a name="add-urlacl"></a>add urlacl

Reserva la dirección URL especificada para usuarios y cuentas que no son administradores. La lista de control de acceso discrecional (DACL) se puede especificar mediante un nombre de cuenta con los parámetros de escucha y delegado o mediante una cadena de lenguaje de definición de descriptor de seguridad (SDDL).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] cadena**
</dt> <dd>

Especifica la dirección URL completa.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> <dd>

Especifica el nombre del usuario o grupo de usuarios.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes \| no}\]**
</dt> <dd>

Especifica uno de los valores siguientes:

-   sí: permite al usuario registrar direcciones URL. Este es el valor predeterminado.
-   no: deniega al usuario el registro de direcciones URL.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes \| no}\]**
</dt> <dd>

Especifica uno de los valores siguientes:

-   sí: permite al usuario delegar direcciones URL.
-   no: deniega al usuario la delegación de direcciones URL. Este es el valor predeterminado.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> <dd>

Especifica la cadena SDDL que describe la DACL.

</dd> </dl>

## <a name="examples"></a>Ejemplos

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Consulte también

* [Comandos http Netsh](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 