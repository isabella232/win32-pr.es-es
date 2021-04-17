---
description: Contiene los parámetros de configuración de EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667663"
---
# <a name="eapol_intf_params-structure"></a>Estructura de los parámetros de Intf de EAPOL \_ \_

\[**EAPOL \_ Los \_ parámetros de Intf** ya no se admiten a partir de Windows Vista y windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

Contiene los parámetros de configuración de EAPOL.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

Versión del autor de la llamada. El valor predeterminado es 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**dwEapFlags**
</dt> <dd>

No se utiliza.

</dd> <dt>

**dwEapType**
</dt> <dd>

Tipo de extensión EAP que se va a usar. Establézcalo en 0x00000013 para EAP-TLS y 0x00000026 para PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Tamaño del identificador de red.

</dd> <dt>

**bSSID**
</dt> <dd>

Identificador de red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El archivo de encabezado wzcsapi. h no está disponible en el Windows SDK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




