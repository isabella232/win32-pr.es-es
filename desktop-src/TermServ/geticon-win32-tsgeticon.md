---
title: Método GetIcon de la Win32_TSGetIcon clase
description: Devuelve el contenido del icono especificado.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Método GetIcon Servicios de Escritorio remoto
- Método GetIcon Servicios de Escritorio remoto , Win32_TSGetIcon clase
- Win32_TSGetIcon clase Servicios de Escritorio remoto , método GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305316d66ce95659210396a10f22366d64ebdd2b410b056aa3c398cf65edbbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001543"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Método GetIcon de la clase \_ TSGetIcon win32

Devuelve el contenido del icono especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FilePath* \[ En\]
</dt> <dd>

Especifica la ruta de acceso al archivo que contiene el icono.

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Especifica el índice del icono en el archivo.

</dd> <dt>

*IconoContents* \[ out\]
</dt> <dd>

Si la finalización se realiza correctamente, contiene el contenido del icono.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGetIcon**](win32-tsgeticon.md)
</dt> </dl>

 

 





