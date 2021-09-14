---
description: Contiene parámetros de configuración eapol.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS estructura (Wzcsapi.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071606"
---
# <a name="eapol_intf_params-structure"></a>Estructura \_ DE EAPOL INTF \_ PARAMS

\[**EAPOL \_ INTF \_ PARAMS** ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [la API Wi-Fi nativa,](native-wifi-reference.md)que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

Contiene parámetros de configuración eapol.

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



## <a name="members"></a>Members

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

Tipo de extensión EAP que se va a usar. Establezca en 0x00000013 para EAP-TLS y 0x00000026 para PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Tamaño del identificador de red.

</dd> <dt>

**Bssid**
</dt> <dd>

Identificador de red.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El archivo de encabezado wzcsapi.h no está disponible en Windows SDK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



 

 




