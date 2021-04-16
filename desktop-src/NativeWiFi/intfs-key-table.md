---
description: Contiene la tabla de información clave para todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: INTFS_KEY_TABLE estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666582"
---
# <a name="intfs_key_table-structure"></a>Estructura de la tabla de claves de INTFS \_ \_

\[**INTFS \_ La \_ tabla de claves** ya no se admite en Windows Vista y windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

La estructura de la **\_ \_ tabla de claves de INTFS** contiene la tabla de información de claves para todas las interfaces de LAN inalámbricas administradas por el servicio de configuración inalámbrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

Número total de interfaces.

</dd> <dt>

**pIntfs**
</dt> <dd>

Puntero a la estructura de [**\_ \_ entrada de la clave Intf**](intf-key-entry.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado *wzcsapi. h* no está disponible en el Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




