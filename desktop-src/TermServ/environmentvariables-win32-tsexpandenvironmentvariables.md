---
title: Método EnvironmentVariables de la Win32_TSExpandEnvironmentVariables clase
description: Expande las variables de entorno definidas por el sistema. | Método EnvironmentVariables de la Win32_TSExpandEnvironmentVariables clase
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Método EnvironmentVariables Servicios de Escritorio remoto
- Método EnvironmentVariables Servicios de Escritorio remoto , Win32_TSExpandEnvironmentVariables clase
- Win32_TSExpandEnvironmentVariables clase Servicios de Escritorio remoto método , EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353897"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Método EnvironmentVariables de la \_ clase TSExpandEnvironmentVariables de Win32

Expande las variables de entorno definidas por el sistema.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OriginalString* \[ En\]
</dt> <dd>

Cadena que contiene las variables de entorno que se expandirán.

</dd> <dt>

*ExpandedString* \[ out\]
</dt> <dd>

Cadena con las variables de entorno expandida.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSExpandEnvironmentVariables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

