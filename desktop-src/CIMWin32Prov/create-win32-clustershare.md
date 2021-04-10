---
description: Crea una nueva instancia de ClusterShare de Win32 \_ .
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Método Create de la clase Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153512"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Método Create de la \_ clase Win32 ClusterShare

Crea una nueva instancia de [**\_ ClusterShare de Win32**](win32-clustershare.md) .

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

*Ruta de acceso* \[ de\]
</dt> <dd>

Ruta de acceso local del recurso compartido de Windows.

Ejemplo, "C: \\ archivos de programa".

</dd> <dt>

*Nombre* \[ de de\]
</dt> <dd>

El alias de una ruta de acceso configurada como un recurso compartido en un equipo con Windows.

Ejemplo, "Public".

</dd> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Tipo de recurso que se va a compartir. Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.

<dt>

0 (0X0)
</dt> <dd>

Unidad de disco

</dd> <dt>

1 (0x1)
</dt> <dd>

Cola de impresión

</dd> <dt>

2 (0X2)
</dt> <dd>

Dispositivo

</dd> <dt>

3 (0X3)
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

Administración de IPC

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[ en, opcional\]
</dt> <dd>

Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.

</dd> <dt>

*Descripción* \[ de en, opcional\]
</dt> <dd>

Descripción del objeto.

</dd> <dt>

*Contraseña* \[ de en, opcional\]
</dt> <dd>

TBD

</dd> <dt>

*Acceso a* \[ en, opcional\]
</dt> <dd>

Instancia integrada opcional de una [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) que contiene el descriptor de seguridad para el nuevo recurso compartido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ ClusterShare**](win32-clustershare.md)
</dt> </dl>

 

