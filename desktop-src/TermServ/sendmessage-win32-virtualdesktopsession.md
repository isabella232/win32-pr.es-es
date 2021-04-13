---
title: Método SendMessage de la clase Win32_VirtualDesktopSession
description: Envíe un mensaje al usuario a través de la sesión de escritorio virtual.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Método SendMessage Servicios de Escritorio remoto
- Método SendMessage Servicios de Escritorio remoto, clase Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession de clase Servicios de Escritorio remoto, método SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422270"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Método SendMessage de la \_ clase Win32 VirtualDesktopSession

Envíe un mensaje al usuario a través de la sesión de escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Título* \[ de de\]
</dt> <dd>

Título de los.

</dd> <dt>

*Mensaje* \[ de de\]
</dt> <dd>

Contenido del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ VirtualDesktopSession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





