---
description: Almacena la información clave sobre una interfaz de LAN inalámbrica administrada por el servicio de configuración inalámbrica.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY estructura (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071597"
---
# <a name="intf_key_entry-structure"></a>Estructura INTF \_ KEY \_ ENTRY

\[**INTF \_ KEY \_ ENTRY** ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [native Wifi API](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API de Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **estructura INTF \_ KEY \_ ENTRY** almacena la información clave sobre una interfaz LAN inalámbrica administrada por el servicio de configuración inalámbrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**wszGuid**
</dt> <dd>

Puntero al GUID de interfaz representado como una cadena Unicode con el siguiente formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* no está disponible en el SDK Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TABLA DE CLAVES \_ \_ INTFS**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




