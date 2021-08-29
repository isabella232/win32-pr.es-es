---
title: Método SetProvider de la Win32_SessionDirectoryVMMPlugin clase
description: Establece el nombre del proveedor de complementos.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Método SetProvider Servicios de Escritorio remoto
- Método SetProvider Servicios de Escritorio remoto , Win32_SessionDirectoryVMMPlugin clase
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto , método SetProvider
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a35bccad8421a47e50e6b7a39e7a259852d90af12452056a604f742ad817d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987695"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetProvider de la clase \_ SessionDirectoryVMMPlugin de Win32

Establece el nombre del proveedor de complementos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sProvider* \[ En\]
</dt> <dd>

Nombre del proveedor del complemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





