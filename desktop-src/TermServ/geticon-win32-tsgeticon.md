---
title: Método GetIcon de la clase Win32_TSGetIcon
description: Devuelve el contenido del icono especificado.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Método GetIcon Servicios de Escritorio remoto
- Método GetIcon Servicios de Escritorio remoto, clase Win32_TSGetIcon
- Win32_TSGetIcon de clase Servicios de Escritorio remoto, método GetIcon
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
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996019"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Método GetIcon de la \_ clase TSGetIcon de Win32

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

*FilePath* \[ de\]
</dt> <dd>

Especifica la ruta de acceso al archivo que contiene el icono.

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

Especifica el índice del icono en el archivo.

</dd> <dt>

*IconContents* \[ enuncia\]
</dt> <dd>

Al finalizar correctamente, se incluye el contenido del icono.

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

[**Win32 \_ TSGetIcon**](win32-tsgeticon.md)
</dt> </dl>

 

 





