---
title: WMDM_SESSION_TYPE enumeración
description: El tipo de \_ enumeración WMDM SESSION \_ TYPE define el tipo de sesión.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE enumeración windows Media Administrador de dispositivos
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
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055533"
---
# <a name="wmdm_session_type-enumeration"></a>Enumeración \_ WMDM SESSION \_ TYPE

El **tipo de \_ enumeración WMDM SESSION \_ TYPE** define el tipo de sesión.

## <a name="syntax"></a>Syntax


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

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ SESSION \_ NONE**
</dt> <dd>

La sesión no está definida.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**TRANSFERENCIA DE SESIÓN DE WMDM \_ \_ AL \_ \_ DISPOSITIVO**
</dt> <dd>

La sesión se define como la transferencia de datos al dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**TRANSFERENCIA DE SESIÓN DE WMDM \_ \_ DESDE EL \_ \_ DISPOSITIVO**
</dt> <dd>

La sesión se define como la transferencia de datos desde el dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM \_ SESSION \_ DELETE**
</dt> <dd>

La sesión se define como la eliminación de datos.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM \_ SESSION \_ CUSTOM**
</dt> <dd>

La sesión se define como una sesión personalizada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tipos de enumeración**](enumeration-types.md)
</dt> </dl>

 

 





