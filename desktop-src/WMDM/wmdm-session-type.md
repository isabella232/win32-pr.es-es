---
title: Enumeración WMDM_SESSION_TYPE
description: El tipo \_ de \_ enumeración de tipo de sesión WMDM define el tipo de sesión.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Enumeración WMDM_SESSION_TYPE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698736"
---
# <a name="wmdm_session_type-enumeration"></a>\_Enumeración de tipo de sesión WMDM \_

El tipo de enumeración de **\_ \_ tipo de sesión WMDM** define el tipo de sesión.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**sesión de WMDM \_ \_ ninguno**
</dt> <dd>

La sesión no está definida.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_ \_ transferencia de sesión \_ de WMDM al \_ dispositivo**
</dt> <dd>

La sesión se define como la transferencia de datos al dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transferencia de sesión \_ de WMDM desde el \_ dispositivo**
</dt> <dd>

La sesión se define como la transferencia de datos desde el dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_eliminación de sesión de WMDM \_**
</dt> <dd>

La sesión se define como la eliminación de datos.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**sesión de WMDM \_ \_ personalizada**
</dt> <dd>

La sesión se define como una sesión personalizada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





