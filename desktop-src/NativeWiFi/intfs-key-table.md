---
description: Contiene la tabla de información clave de todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: INTFS_KEY_TABLE estructura (Wzcsapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071596"
---
# <a name="intfs_key_table-structure"></a>Estructura INTFS \_ KEY \_ TABLE

\[**INTFS \_ KEY \_ TABLE** ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [la API Wi-Fi nativa,](native-wifi-reference.md)que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **estructura INTFS \_ KEY \_ TABLE** contiene la tabla de información clave de todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

Número total de interfaces.

</dd> <dt>

**pIntfs**
</dt> <dd>

Puntero a la [**estructura INTF \_ KEY \_ ENTRY.**](intf-key-entry.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* no está disponible en el SDK Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



 

 




