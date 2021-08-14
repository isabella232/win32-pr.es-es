---
title: Atributo ms-DS-Has-Instantiated-NCs
description: Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes tieneMasterNCs y hasPartialReplicaNCs. Para que la KCC la utilice al configurar asociados de replicación.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Has-Instantiated-NCs
- Esquema de AD del atributo msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efde9ef1cd9a7230e4493d3e542e1f5f661ed33027ad3e9a88ded9679df812c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804064"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>Atributo ms-DS-Has-Instantiated-NCs

Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes tieneMasterNCs y hasPartialReplicaNCs. Para que la KCC la utilice al configurar asociados de replicación.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Has-Instantiated-NCs                                                                                                                                                                                  |
| Ldap-Display-Name | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Size              | 4 bytes                                                                                                                                                                                                     |
| Privilegio actualizar  | El sistema establece este valor.                                                                                                                                                                            |
| Frecuencia de actualización  | Aproximadamente el doble de frecuencia que hasMasterNCs/hasPartialReplicaNCs. Estos atributos existentes solo se actualizan cuando el controlador de dominio agrega o quita una partición (por ejemplo, al cambiar de DC a GC o viceversa). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-Id-Guid    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------|
| Id. de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | Verdadero                                     |
| Es de un solo valor       | Falso                                    |
| Está indexado             | Falso                                    |
| En el catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





