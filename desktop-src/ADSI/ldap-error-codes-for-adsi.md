---
title: Códigos de error LDAP para ADSI
description: Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP convierte el error en una cadena.
ms.assetid: 7a0a5a1b-8473-405b-a590-3f917e50cbdc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149abf4562b0e35067149fb69c9a1ec1304cc528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174570"
---
# <a name="ldap-error-codes-for-adsi"></a>Códigos de error LDAP para ADSI

Cuando un servidor LDAP genera un error y pasa el error al cliente, el cliente LDAP convierte el error en una cadena.

Este método es similar a los [códigos de error de Win32 para ADSI.](win32-error-codes-for-adsi.md) En este ejemplo, el código de error del cliente es el error de WIN32 0x80072020.

**Para determinar los códigos de error LDAP para ADSI**

1.  Quitar el 8007 del código de error de WIN32. En el ejemplo, el valor hexadecimal restante es 2020.
2.  Convierta el valor hexadecimal restante en un valor decimal. En el ejemplo, el valor hexadecimal 2020 restante se convierte en el valor decimal 8224.
3.  Busque en el archivo WinError.h la definición del valor decimal. En el ejemplo, 8224L corresponde al error **ERROR \_ DS \_ OPERATIONS \_ ERROR**.
4.  Reemplace el prefijo **ERROR \_ DS** por **\_ LDAP.** En el ejemplo, la nueva definición es **LDAP \_ OPERATIONS \_ ERROR**.
5.  Busque en el archivo Winldap.h el valor de la definición de error ldap. En el ejemplo, el valor de **LDAP \_ OPERATIONS \_ ERROR** en el archivo Winldap.h es 0x01.

 

 




