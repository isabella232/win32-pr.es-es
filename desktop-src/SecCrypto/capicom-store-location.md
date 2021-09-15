---
description: Indica la ubicación de un almacén de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476524"
---
# <a name="capicom_store_location-enumeration"></a>ENUMERACIÓN CAPICOM \_ STORE \_ LOCATION

El **tipo de enumeración \_ CAPICOM STORE \_ LOCATION** indica la ubicación de un almacén [*de certificados.*](../secgloss/c-gly.md)

## <a name="members"></a>Members



| Miembro                                      | Descripción                                                                                                                                                                                                                                                                      | Value |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **ALMACÉN DE MEMORIA \_ CAPICOM \_**                  | El almacén es un almacén de memoria. Los cambios en el contenido del almacén no se conservan.<br/>                                                                                                                                                                              | 0     |
| **CAPICOM \_ LOCAL \_ MACHINE \_ STORE**          | El almacén es un almacén de máquina local. Los almacenes de máquinas locales solo pueden ser almacenes de lectura y escritura si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si se abre el almacén de lectura y escritura, se conservan los cambios en el contenido del almacén.<br/> | 1     |
| **ALMACÉN DE USUARIOS \_ ACTUAL DE CAPICOM \_ \_**           | El almacén es un almacén de usuario actual. Un almacén de usuarios actual puede ser un almacén de lectura y escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                      | 2     |
| **ALMACÉN DE USUARIOS \_ DE CAPICOM ACTIVE \_ DIRECTORY \_ \_** | El almacén es un Active Directory almacén. Active Directory se pueden abrir solo en modo de solo lectura. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                                                                                        | 3     |
| **ALMACÉN DE USUARIOS \_ DE TARJETA \_ INTELIGENTE \_ CAPICOM \_**       | Los almacenes admiten almacenes de certificados basados en tarjetas inteligentes. La tienda es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2.0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Observaciones

Los métodos siguientes usan el tipo de enumeración **\_ CAPICOM STORE \_ LOCATION:**

-   [**PrivateKey.Open**](privatekey-open.md)
-   [**Store.Open**](store-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
