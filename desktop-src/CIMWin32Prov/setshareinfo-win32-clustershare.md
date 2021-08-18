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
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439405"
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

*MaximumAllowed* \[ en, opcional\]
</dt> <dd>

Limite el número máximo de usuarios que pueden usar este recurso simultáneamente.

</dd> <dt>

*Descripción* \[ en, opcional\]
</dt> <dd>

Describe el recurso que se comparte.

</dd> <dt>

*Acceso* \[ en, opcional\]
</dt> <dd>

Descriptor de seguridad para permisos de nivel de usuario. Un descriptor de seguridad contiene información sobre las funcionalidades de permiso, propietario y acceso del recurso. Para obtener más información, [**vea Seguridad de Win32Descriptor. \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ClusterShare de Win32 \_**](win32-clustershare.md)
</dt> </dl>

 

