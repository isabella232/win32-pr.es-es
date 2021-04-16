---
title: Método EnvironmentVariables de la clase Win32_TSExpandEnvironmentVariables
description: Expande las variables de entorno definidas por el sistema. | Método EnvironmentVariables de la clase Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Método EnvironmentVariables Servicios de Escritorio remoto
- Método EnvironmentVariables Servicios de Escritorio remoto, clase Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables de clase Servicios de Escritorio remoto, método EnvironmentVariables
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
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678685"
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

*OriginalString* \[ de\]
</dt> <dd>

Cadena que contiene las variables de entorno que se van a expandir.

</dd> <dt>

*ExpandedString* \[ enuncia\]
</dt> <dd>

Una cadena con las variables de entorno expandidas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSExpandEnvironmentVariables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

