---
description: El método Reset de la clase \_ Cim FlatPanel solicita un restablecimiento del dispositivo lógico.
ms.assetid: 098d6fe9-ae13-495d-a579-d1eb0157688e
ms.tgt_platform: multiple
title: Método Reset de la CIM_FlatPanel clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5961a144e30ca8b28bbf90ea7a4ceec2372048273ea7ae5f3ed9791d353984ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119218085"
---
# <a name="reset-method-of-the-cim_flatpanel-class"></a>Método Reset de la clase \_ FlatPanel cim

El **método Reset** de la clase Cim \_ FlatPanel solicita un restablecimiento del dispositivo lógico. Este método se hereda de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[CIM \_ FlatPanel](reset-method-in-class-cim-flatpanel.md)
</dt> <dt>

[**CIM \_ FlatPanel**](cim-flatpanel.md)
</dt> </dl>

 

 




