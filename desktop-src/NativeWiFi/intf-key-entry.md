---
description: Almacena la información clave sobre una interfaz LAN inalámbrica administrada por el servicio de configuración inalámbrica.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY estructura (wzcsapi. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360378"
---
# <a name="intf_key_entry-structure"></a>Estructura de entrada de \_ clave de Intf \_

\[**Intf \_ La \_ entrada de clave** ya no se admite en Windows Vista y windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

La estructura de **\_ \_ entrada de clave de Intf** almacena la información clave sobre una interfaz LAN inalámbrica administrada por el servicio de configuración inalámbrica.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wszGuid**
</dt> <dd>

Puntero al GUID de la interfaz que se representa como una cadena Unicode en el siguiente formato: "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tabla de claves de INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




