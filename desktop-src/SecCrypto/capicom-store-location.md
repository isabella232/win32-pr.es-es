---
description: Indica la ubicación de un almacén de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumeración CAPICOM_STORE_LOCATION (CAPICOM. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671365"
---
# <a name="capicom_store_location-enumeration"></a>\_Enumeración de ubicación del almacén de CAPICOM \_

El tipo de enumeración **\_ \_ Ubicación del almacén de CAPICOM** indica la ubicación de un almacén de [*certificados*](../secgloss/c-gly.md).

## <a name="members"></a>Miembros



| Miembro                                      | Descripción                                                                                                                                                                                                                                                                      | Value |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_almacén de memoria CAPICOM \_**                  | El almacén es un almacén de memoria. No se conservan los cambios en el contenido del almacén.<br/>                                                                                                                                                                              | 0     |
| **\_almacén del \_ equipo \_ local de CAPICOM**          | El almacén es un almacén del equipo local. Los almacenes de máquinas locales pueden ser almacenes de lectura y escritura solo si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si el almacén está abierto para lectura y escritura, se conservan los cambios en el contenido del almacén.<br/> | 1     |
| **\_almacén de \_ usuarios \_ actual de CAPICOM**           | El almacén es un almacén de usuario actual. Un almacén de usuario actual puede ser un almacén de lectura/escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                      | 2     |
| **el \_ \_ almacén de \_ usuarios de Active \_ Directory de CAPICOM** | El almacén es un almacén de Active Directory. Active Directory almacenes solo se pueden abrir en modo de solo lectura. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                                                                                        | 3     |
| **el \_ \_ almacén de \_ usuarios de tarjetas inteligentes CAPICOM \_**       | Los almacenes admiten almacenes de certificados basados en tarjetas inteligentes. El almacén es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2,0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Observaciones

Los métodos siguientes utilizan el tipo de enumeración de **\_ \_ Ubicación de almacén de CAPICOM** :

-   [**PrivateKey. Open**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
