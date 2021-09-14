---
title: Método SetProgramList de la Win32_TSVirtualIP clase
description: Sobrescribe la lista de programas que usan la virtualización de IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Método SetProgramList Servicios de Escritorio remoto
- Método SetProgramList Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto método , SetProgramList
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253281"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Método SetProgramList de la clase \_ TSVirtualIP de Win32

Sobrescribe la lista de programas que usan la virtualización de IP.

## <a name="syntax"></a>Sintaxis


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProgramList* \[ En\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz de cadenas que contienen la ruta de acceso y los nombres de archivo de los programas que usan la virtualización ip.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **unint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSVirtualIP de Win32 \_**](win32-tsvirtualip.md)
</dt> </dl>

 

 





