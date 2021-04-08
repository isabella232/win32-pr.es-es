---
title: add urlacl
description: Reserva la URL especificada para las cuentas y los usuarios que no son administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Agregar urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104003751"
---
# <a name="add-urlacl"></a>add urlacl

Reserva la URL especificada para las cuentas y los usuarios que no son administradores. La lista de control de acceso discrecional (DACL) se puede especificar mediante el uso de un nombre de cuenta con los parámetros Listen y Delegate o mediante una cadena de lenguaje de definición de descriptores de seguridad (SDDL).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] cadena**
</dt> <dd>

Especifica la dirección URL completa.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] cadena**
</dt> <dd>

Especifica el nombre del usuario o del grupo de usuarios.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[Listen = {sí \| no}\]**
</dt> <dd>

Especifica uno de los siguientes valores:

-   sí: permite al usuario registrar las direcciones URL. Este es el valor predeterminado.
-   no: deniega al usuario el registro de las direcciones URL.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegado = {sí \| no}\]**
</dt> <dd>

Especifica uno de los siguientes valores:

-   sí: permite que el usuario delegue las direcciones URL.
-   no: deniega al usuario que delegue las direcciones URL. Este es el valor predeterminado.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] cadena**
</dt> <dd>

Especifica la cadena SDDL que describe la DACL.

</dd> </dl>

## <a name="examples"></a>Ejemplos

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Consulte también

* [Comandos http Netsh](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 