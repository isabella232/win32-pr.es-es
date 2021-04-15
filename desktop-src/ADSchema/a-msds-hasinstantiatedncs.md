---
title: atributo MS-DS-ha-created-NC
description: Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes hasMasterNCs y hasPartialReplicaNCs. Que va a usar el KCC al configurar los asociados de replicación.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- MS-DS-ha-created-NC atributo AD Schema
- Esquema de AD de atributo msDS-HasInstantiatedNCs
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493822"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>atributo MS-DS-ha-created-NC

Información de estado de replicación de DS, análoga a (y un superconjunto de) los atributos existentes hasMasterNCs y hasPartialReplicaNCs. Que va a usar el KCC al configurar los asociados de replicación.



| Entrada | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-se ha creado una instancia-NC                                                                                                                                                                                  |
| Nombre para mostrar de LDAP | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Tamaño              | 4 bytes                                                                                                                                                                                                     |
| Actualizar privilegio  | El sistema establece este valor.                                                                                                                                                                            |
| Frecuencia de actualización  | Casi el doble de la frecuencia que hasMasterNCs/hasPartialReplicaNCs. Estos atributos existentes solo se actualizan cuando el controlador de dominio agrega o quita una partición (por ejemplo, al cambiar de DC a GC o viceversa). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-ID-GUID    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Sintaxis            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| Tiene un único valor       | False                                    |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





