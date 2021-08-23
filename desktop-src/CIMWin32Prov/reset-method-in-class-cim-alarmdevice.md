---
description: El método Reset de la clase \_ CIM AlarmDevice solicita un restablecimiento de dispositivo lógico. Este método se hereda de \_ CIM LogicalDevice.
ms.assetid: e70718c5-2c80-4084-b233-b3e4d083e7b4
ms.tgt_platform: multiple
title: Método Reset de la CIM_AlarmDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac0cd1ded976ed4ba28ca89715d9ba72ea6c324b6eaaadc71eff8a38ca8f827e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816685"
---
# <a name="reset-method-of-the-cim_alarmdevice-class"></a>Método Reset de la clase \_ AlarmDevice de CIM

El **método Reset** de la clase CIM [**\_ AlarmDevice**](cim-alarmdevice.md) solicita un restablecimiento de dispositivo lógico. Este método se hereda de [**\_ CIM LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y algún otro valor si se produjo un error.

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[CIM \_ AlarmDevice](reset-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> </dl>

 

 




