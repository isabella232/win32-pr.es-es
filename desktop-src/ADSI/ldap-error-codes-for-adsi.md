---
title: Códigos de error LDAP para ADSI
description: Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP traduce el error a una cadena.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903044"
---
# <a name="ldap-error-codes-for-adsi"></a>Códigos de error LDAP para ADSI

Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP traduce el error a una cadena.

Este método es similar a los [códigos de error de Win32 para ADSI](win32-error-codes-for-adsi.md). En este ejemplo, el código de error de cliente es el error 0x80072020 de WIN32.

**Para determinar los códigos de error LDAP para ADSI**

1.  Quite 8007 del código de error de WIN32. En el ejemplo, el valor hexadecimal restante es 2020.
2.  Convierta el valor hexadecimal restante en un valor decimal. En el ejemplo, el valor hexadecimal restante 2020 se convierte en el valor decimal 8224.
3.  Busque en el archivo WinError. h la definición del valor decimal. En el ejemplo, 8224L corresponde al error de error de **\_ \_ las \_ operaciones de DS**.
4.  Reemplace el prefijo **\_ DS de error** por **LDAP \_**. En el ejemplo, la nueva definición es **\_ \_ error de operaciones LDAP**.
5.  Busque el valor de la definición de error LDAP en el archivo Winldap. h. En el ejemplo, el valor de **\_ \_ error de operaciones LDAP** en el archivo Winldap. h es 0x01.

 

 




