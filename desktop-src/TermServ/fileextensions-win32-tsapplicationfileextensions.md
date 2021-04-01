---
title: Método FileExtensions de la clase Win32_TSApplicationFileExtensions
description: Proporciona una lista de las extensiones de nombre de archivo controladas por una aplicación.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Método FileExtensions Servicios de Escritorio remoto
- Método FileExtensions Servicios de Escritorio remoto, clase Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de clase Servicios de Escritorio remoto, método FileExtensions
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
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996990"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileExtensions de la \_ clase TSApplicationFileExtensions de Win32

Proporciona una lista de las extensiones de nombre de archivo controladas por una aplicación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppPath* \[ de\]
</dt> <dd>

Ruta de acceso de la aplicación.

</dd> <dt>

*Extensiones* \[ de enuncia\]
</dt> <dd>

Extensiones de nombre de archivo controladas por la aplicación.

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

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

