---
description: Crea una nueva instancia de \_ ClusterShare de Win32.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Método Create de la Win32_ClusterShare clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020593"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Método Create de la clase ClusterShare de Win32 \_

Crea una nueva [**instancia de \_ ClusterShare de Win32.**](win32-clustershare.md)

## <a name="syntax"></a>Sintaxis


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* \[ En\]
</dt> <dd>

Ruta de acceso local del recurso Windows compartido.

Ejemplo, "C: \\ Archivos de programa".

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Alias de una ruta de acceso configurada como recurso compartido en un sistema informático que ejecuta Windows.

Ejemplo, "public".

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo de recurso que se comparte. Los tipos incluyen: unidades de disco, colas de impresión, comunicaciones entre procesos (IPC) y dispositivos generales.

<dt>

0 (0x0)
</dt> <dd>

Unidad de disco

</dd> <dt>

1 (0x1)
</dt> <dd>

Cola de impresión

</dd> <dt>

2 (0x2)
</dt> <dd>

Dispositivo

</dd> <dt>

3 (0x3)
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000)
</dt> <dd>

Administrador de unidad de disco

</dd> <dt>

2147483649 (0x80000001)
</dt> <dd>

Administrador de cola de impresión

</dd> <dt>

2147483650 (0x80000002)
</dt> <dd>

Administrador de dispositivos

</dd> <dt>

2147483651 (0x80000003)
</dt> <dd>

Administrador de IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, opcional\]
</dt> <dd>

Limite el número máximo de usuarios que pueden usar este recurso simultáneamente.

</dd> <dt>

*Descripción* \[ in, opcional\]
</dt> <dd>

Descripción del objeto.

</dd> <dt>

*Contraseña* \[ in, opcional\]
</dt> <dd>

Por determinar

</dd> <dt>

*Acceso* \[ in, opcional\]
</dt> <dd>

Instancia incrustada opcional de una [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) que contiene el descriptor de seguridad para el nuevo recurso compartido.

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

 

