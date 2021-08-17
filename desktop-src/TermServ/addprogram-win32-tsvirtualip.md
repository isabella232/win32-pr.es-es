---
title: Método AddProgram de la clase Win32_TSVirtualIP (Bdaiface.h)
description: Agrega un programa a la lista de programas que usan la virtualización IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Método AddProgram Servicios de Escritorio remoto
- Método AddProgram Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto método , AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2f78cb461a61467867a544e954a71c23d59432e29450a7b0f35184f0edec57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757868"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>Método AddProgram de la clase \_ TSVirtualIP de Win32

Agrega un programa a la lista de programas que usan la virtualización IP.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProgramPath* \[ En\]
</dt> <dd>

Tipo: **cadena**

Ruta de acceso y nombre de archivo del programa que se agregará a la lista.

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
| Header<br/>                   | <dl> <dt>Bdaiface.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSVirtualIP de Win32 \_**](win32-tsvirtualip.md)
</dt> </dl>

 

 





