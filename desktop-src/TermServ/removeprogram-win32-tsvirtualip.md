---
title: Método RemoveProgram de la clase Win32_TSVirtualIP (Bdaiface.h)
description: Quita un programa de la lista de programas que usan la virtualización de IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Método RemoveProgram Servicios de Escritorio remoto
- Método RemoveProgram Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto método , RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374582"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a>Método RemoveProgram de la clase \_ TSVirtualIP de Win32

Quita un programa de la lista de programas que usan la virtualización de IP.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProgramPath* \[ En\]
</dt> <dd>

Tipo: **cadena**

Ruta de acceso y nombre de archivo del programa que se quitará de la lista. Si no se encuentra el programa, se devuelve un error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Bdaiface.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSVirtualIP de Win32 \_**](win32-tsvirtualip.md)
</dt> </dl>

 

 





