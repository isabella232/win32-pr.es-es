---
title: Address-Type atributo
description: Cadena de caracteres que describe el formato de la dirección del usuario. Los tipos de direcciones se asignan a formatos de dirección. Es decir, al mirar el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección adecuada para el destinatario.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Address-Type esquema de AD del atributo
- Esquema de AD del atributo addressType
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2ce0ff9651350803a05b3b3bf3dda663419c9948617b706688bf78057ad72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118688492"
---
# <a name="address-type-attribute"></a>Address-Type atributo

Cadena de caracteres que describe el formato de la dirección del usuario. Los tipos de direcciones se asignan a formatos de dirección. Es decir, al mirar el tipo de dirección de un destinatario, las aplicaciones cliente pueden determinar cómo dar formato a una dirección adecuada para el destinatario.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| CN                | Address-Type                                                                                                              |
| Ldap-Display-Name | addressType                                                                                                               |
| Size              | Tipos de direcciones: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN, PROFS,SMTP, SNADS, TELEX, X400, X500 |
| Privilegio actualizar  | El sistema establece este valor.                                                                                          |
| Frecuencia de actualización  | Se establece cuando se crea el objeto.                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.2.350                                                                                                    |
| System-Id-Guid    | 5fd42464-1262-11d0-a060-00aa006c33ed                                                                                      |
| Syntax            | [**String(Teletex)**](s-string-teletex.md)                                                                               |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Verdadero                                                     |
| Está indexado             | Falso                                                    |
| En el catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Plantilla de dirección**](c-addresstemplate.md)<br/> |



 

 





