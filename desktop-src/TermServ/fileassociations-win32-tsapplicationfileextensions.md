---
title: Método FileAssociations de la clase Win32_TSApplicationFileExtensions
description: Examina el registro para obtener las asociaciones de archivo actuales para una aplicación.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método FileAssociations Servicios de Escritorio remoto
- Método FileAssociations Servicios de Escritorio remoto, clase Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de clase Servicios de Escritorio remoto, método FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686182"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileAssociations de la \_ clase TSApplicationFileExtensions de Win32

Examina el registro para obtener las asociaciones de archivo actuales para una aplicación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppPath* \[ de\]
</dt> <dd>

Especifica la ruta de acceso a la aplicación.

</dd> <dt>

*FileAssociations* \[ enuncia\]
</dt> <dd>

Al finalizar correctamente contiene las asociaciones de archivo para esta aplicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ RDFileAssociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 





