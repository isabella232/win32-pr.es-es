---
title: Método FileExtensions de la Win32_TSApplicationFileExtensions clase
description: Proporciona una lista de las extensiones de nombre de archivo que administra una aplicación.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Método FileExtensions Servicios de Escritorio remoto
- Método FileExtensions Servicios de Escritorio remoto , Win32_TSApplicationFileExtensions clase
- Win32_TSApplicationFileExtensions clase Servicios de Escritorio remoto método , FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609377"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileExtensions de la clase \_ TSApplicationFileExtensions de Win32

Proporciona una lista de las extensiones de nombre de archivo que administra una aplicación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppPath* \[ En\]
</dt> <dd>

Ruta de acceso de la aplicación.

</dd> <dt>

*Extensiones* \[ out\]
</dt> <dd>

Las extensiones de nombre de archivo que controla la aplicación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSApplicationFileExtensions de Win32 \_**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

