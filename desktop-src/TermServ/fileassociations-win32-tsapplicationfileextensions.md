---
title: Método FileAssociations de la Win32_TSApplicationFileExtensions clase
description: Examina el Registro para obtener las asociaciones de archivo actuales de una aplicación.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Método FileAssociations Servicios de Escritorio remoto
- Método FileAssociations Servicios de Escritorio remoto , Win32_TSApplicationFileExtensions clase
- Win32_TSApplicationFileExtensions clase Servicios de Escritorio remoto método , FileAssociations
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
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737515"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Método FileAssociations de la clase \_ TSApplicationFileExtensions de Win32

Examina el Registro para obtener las asociaciones de archivo actuales de una aplicación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppPath* \[ En\]
</dt> <dd>

Especifica la ruta de acceso a la aplicación.

</dd> <dt>

*FileAssociations* \[ out\]
</dt> <dd>

Si la finalización se realiza correctamente, contiene las asociaciones de archivo para esta aplicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSApplicationFileExtensions de Win32 \_**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**RdFileAssociation de Win32 \_**](win32-rdfileassociation.md)
</dt> </dl>

 

 





