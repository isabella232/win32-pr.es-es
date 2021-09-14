---
description: Establece los parámetros del recurso compartido.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Método SetShareInfo de la Win32_ClusterShare clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970287"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Método SetShareInfo de la clase ClusterShare de Win32 \_

Establece los parámetros del recurso compartido.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaximumAllowed* \[ in, opcional\]
</dt> <dd>

Limite el número máximo de usuarios que pueden usar este recurso simultáneamente.

</dd> <dt>

*Descripción* \[ in, opcional\]
</dt> <dd>

Describe el recurso que se comparte.

</dd> <dt>

*Acceso* \[ in, opcional\]
</dt> <dd>

Descriptor de seguridad para permisos de nivel de usuario. Un descriptor de seguridad contiene información sobre las funcionalidades de permiso, propietario y acceso del recurso. Para más información, consulte [**Seguridad de Win32Descriptor. \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ClusterShare de Win32 \_**](win32-clustershare.md)
</dt> </dl>

 

